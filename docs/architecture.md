# Architecture SI initiale (livrable B)

> **v0 à valider par Matthieu Baric.** Ébauche rédigée avec Claude à partir de la fiche de cadrage V5 et du benchmark. Elle sera approfondie pour le dépôt 2 du 13/11.

## Principes

1. **Les fonctions réglementées sont confiées à des partenaires agréés.** Billes garde l'expérience, le coach et la relation client.
2. **Les prestataires sont interchangeables.** Chaque partenaire est appelé à travers un adaptateur, pour éviter le scénario Kard, liquidé après la rupture de contrat de son prestataire.
3. **Le portefeuille fonctionne sans l'IA.** Un don aboutit même si le coach est indisponible : le coach réagit à un événement et ne bloque jamais le transfert.
4. **Les données partagées sont séparées des données privées.** Le service de partage ne lit jamais le détail des opérations.
5. **Le modèle d'IA ne reçoit que des données pseudonymisées.** Aucun libellé de transaction ne lui est envoyé en clair.

## Composants, services, API et stockage

Dans le projet, tous les partenaires externes sont **simulés** par des bouchons.

```mermaid
flowchart TB
    subgraph Client
        APP["Application mobile et web<br/>Mode accessibilité, voix ou texte"]
    end

    GW["Passerelle API<br/>Authentification, limites de débit"]

    subgraph Billes["Services Billes"]
        AUTH["Comptes et authentification"]
        CONS["Consentements"]
        WALLET["Portefeuille<br/>Solde, opérations, statuts"]
        DON["Dons et cartes cadeaux"]
        AGG["Vue consolidée"]
        COACH["Coach IA<br/>Pseudonymisation, RAG, filtres de sortie"]
        SHARE["Partage familial"]
        NOTIF["Notifications"]
    end

    BUS(["Bus d'événements"])

    subgraph Stockage
        DB[("Base relationnelle<br/>Comptes, opérations, consentements")]
        VEC[("Base vectorielle<br/>Contenus pédagogiques validés")]
        LOG[("Journal d'audit")]
    end

    subgraph Partenaires["Partenaires externes, simulés dans le projet"]
        BAAS["Banking-as-a-Service<br/>Adaptateur paiement"]
        AIS["Agrégateur DSP2<br/>Adaptateur agrégation"]
        LLM["Modèle d'IA hébergé en UE"]
        VOICE["Transcription et synthèse vocale"]
    end

    APP --> GW
    GW --> AUTH & CONS & WALLET & DON & AGG & COACH & SHARE
    DON --> WALLET
    WALLET --> BAAS
    AGG --> AIS
    AGG --> CONS
    SHARE --> CONS
    COACH --> LLM
    COACH --> VOICE
    COACH --> VEC
    WALLET -- "operation.validee" --> BUS
    BUS --> COACH
    BUS --> NOTIF
    AUTH & CONS & WALLET & DON & AGG & SHARE --> DB
    WALLET & CONS & COACH --> LOG
```

### API principales (premières pistes)

| Méthode et route | Rôle | Fonction imposée |
|---|---|---|
| `POST /auth/inscription`, `POST /auth/connexion` | Créer un compte, s'authentifier | 1 |
| `GET /comptes/vue-consolidee` | Soldes des comptes externes et du compte Billes | 2 |
| `GET /operations` | Historique catégorisé | 2 |
| `POST /rechargements` | Rechargement par carte fictive ou code de carte cadeau | 3 |
| `POST /dons` | Coup de pouce, avec clé d'idempotence | 4 |
| `GET /operations/{id}` | Statut et cause d'échec | 5 |
| `GET` et `PUT /securite/parametres` | Plafonds, appareils, mode accessibilité | 6 |
| `GET` et `PUT /consentements` | Agrégation, IA, partage familial | 6 |
| `GET /coach/plans/{donId}`, `POST /coach/plans/{donId}/decision` | Consulter le plan, décider | Coach IA |

## Flux d'un transfert, nominal et échec

```mermaid
sequenceDiagram
    actor B as Bernard
    participant A as Application
    participant W as Portefeuille
    participant P as Partenaire paiement (simulé)
    participant E as Bus d'événements
    participant C as Coach IA
    actor L as Léa

    B->>A: Envoie 50 € pour le permis
    A->>W: POST /dons avec clé d'idempotence
    W->>W: Contrôle solde, plafond et bénéficiaire
    alt Contrôle refusé
        W-->>A: Échouée, cause en langage simple
        A-->>B: Solde insuffisant ou plafond atteint, et que faire
    else Contrôle accepté
        W->>P: Ordre de transfert, statut En attente
        alt Partenaire accepte
            P-->>W: Confirmation
            W->>W: Écriture débit et crédit, statut Validée
            W-->>A: Validée
            A-->>B: Votre don est arrivé
            W-)E: operation.validee
            E-)C: Préparer un plan
            C-->>L: Plan proposé, avec mention IA
            L->>C: Décide, l'IA ne fait que suggérer
        else Partenaire refuse ou ne répond pas
            P--xW: Refus ou délai dépassé
            W->>W: Aucune écriture, statut Échouée
            W-->>A: Échouée
            A-->>B: Rien n'a été débité, vous pouvez réessayer
        end
    end
```

- **Idempotence** : renvoyer une requête avec la même clé ne crée pas de deuxième don.
- **Coach indisponible** : l'événement reste en file d'attente, le don est déjà validé et le plan arrive plus tard.

### Cycle de vie d'une opération

```mermaid
stateDiagram-v2
    [*] --> EnAttente: Demande acceptée
    [*] --> Echouee: Contrôle refusé
    EnAttente --> Validee: Confirmation du partenaire
    EnAttente --> Echouee: Refus ou délai dépassé
    Validee --> [*]
    Echouee --> [*]
```

## Modèle de données synthétique

```mermaid
erDiagram
    UTILISATEUR ||--o| COMPTE_BILLES : possede
    UTILISATEUR ||--o{ COMPTE_EXTERNE : connecte
    UTILISATEUR ||--o{ CONSENTEMENT : donne
    UTILISATEUR ||--o{ OBJECTIF : fixe
    COMPTE_BILLES ||--o{ OPERATION : enregistre
    COMPTE_EXTERNE ||--o{ OPERATION : synchronise
    DON ||--|| OPERATION : genere
    CARTE_CADEAU |o--o| DON : finance
    DON ||--o| PLAN_COACH : declenche
    PLAN_COACH ||--|{ ENVELOPPE : propose
    OBJECTIF ||--o{ PARTAGE : expose

    UTILISATEUR {
        uuid id PK
        string role
        boolean mode_accessibilite
    }
    COMPTE_BILLES {
        uuid id PK
        uuid utilisateur_id FK
        decimal solde
    }
    COMPTE_EXTERNE {
        uuid id PK
        uuid utilisateur_id FK
        string banque
        date derniere_authentification
    }
    OPERATION {
        uuid id PK
        decimal montant
        string statut
        string cause_echec
        string categorie
        string cle_idempotence
    }
    DON {
        uuid id PK
        uuid donateur_id FK
        uuid beneficiaire_id FK
        string intention
    }
    CARTE_CADEAU {
        uuid id PK
        string code
        decimal montant
        date expiration
    }
    OBJECTIF {
        uuid id PK
        string libelle
        decimal cible
        decimal atteint
    }
    CONSENTEMENT {
        uuid id PK
        string type
        date accorde_le
        date revoque_le
    }
    PARTAGE {
        uuid id PK
        uuid destinataire_id FK
        string niveau
        boolean actif
    }
    PLAN_COACH {
        uuid id PK
        string decision
        string version_contenu
    }
    ENVELOPPE {
        uuid id PK
        string type
        decimal montant
    }
```

## Position de l'IA

| Point | Choix |
|---|---|
| Déclenchement | Asynchrone, après un événement `operation.validee`, ou à la demande de l'utilisateur |
| Entrées | Profil structuré et opérations **pseudonymisées**, sans les données de partage familial |
| Sources du coach | Contenus pédagogiques validés, par RAG |
| Sorties | Filtre bloquant toute recommandation de produit financier, mention IA systématique |
| Décision | Toujours prise par l'utilisateur, aucune action automatique sur le solde |
| Traçabilité | Version du contenu et décision conservées dans `PLAN_COACH`, journal d'audit |
| Voix | Transcription et synthèse uniquement, audio supprimé après traitement, jamais d'identification du locuteur |

## Alternative argumentée : partenaire agréé ou agrément en propre

| Critère | **Partenaire agréé (retenu)** | Agrément d'établissement de monnaie électronique en propre |
|---|---|---|
| Coût d'entrée | À partir de 2 990 €/mois chez Swan, soit 35 880 €/an | 350 000 € de capital, plus une fonction conformité permanente |
| Délai | Quelques mois (à confirmer) | Environ un an de préparation |
| Sécurité et conformité | Le partenaire porte l'essentiel des obligations réglementaires | Maîtrise complète, responsabilité complète |
| Échelle | Dépendance au prestataire, marge partagée | Marge et feuille de route maîtrisées |
| Risque principal | Rupture de contrat, couverte par les adaptateurs et un deuxième prestataire | Coût fixe élevé avant toute traction |

**Choix** : partenaire agréé pour le MVP. L'agrément en propre ne se justifie qu'à grande échelle, voir la [roadmap de financement](annexes-cadrage.md#a3-roadmap-produit-et-financement-projection-illustrative).

## À trancher pour le 13/11

- Monolithe modulaire ou services séparés : le découpage ci-dessus est **logique**. Un seul déployable semble suffisant pour un MVP, à argumenter.
- Choix de l'hébergeur en UE et de la base vectorielle.
- Choix du fournisseur de modèle d'IA, selon le prix et les garanties de non-réutilisation des données.
- Qui gère le renouvellement de l'authentification forte tous les 180 jours : Billes ou l'agrégateur.
