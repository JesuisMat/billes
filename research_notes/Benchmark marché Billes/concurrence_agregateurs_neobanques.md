# Paysage concurrentiel : agrégateurs de comptes et néobanques jeunes/famille (benchmark Racines, état au 30 octobre 2026)

> Périmètre : France d'abord, avec les références UE/UK/US qui comptent. Notes de recherche écrites à partir de sources web consultées le 30/10/2026 via Firecrawl. Chaque chiffre porte sa source et sa date. Les infos antérieures à 2024 sont signalées par **[ANCIEN]**, les fermetures et rachats par **[FERMÉ]** ou **[RACHAT]**. Quand une donnée n'a pas été trouvée, elle est notée « inconnu » et listée dans la partie Gaps : aucun chiffre n'a été inventé.

---

## Q1. Agrégateurs de comptes / PFM en France et en Europe : offre, utilisateurs, prix, modèle économique, fermetures et pivots

### Takeaway
Le marché français de l'agrégation se partage entre trois profils. **Bankin'** est le PFM grand public : freemium, avec une activité B2B via l'API Bridge, il annonce plusieurs millions d'utilisateurs. **Linxo** est aujourd'hui une filiale du Crédit Agricole, tournée à la fois vers le B2C et l'open banking B2B. **Finary** fait du suivi de patrimoine : il annonce plus de 600 k puis plus de 1 M d'utilisateurs, a levé 25 M€ en 2025 et pivote vers le courtage et la gestion de patrimoine avec un « agent IA ». Powens (ex-Budget Insight) et Tink sont des fournisseurs **B2B purs** : ce sont des briques techniques qu'un acteur comme Racines peut utiliser, pas des concurrents directs. Aucun de ces acteurs ne cible explicitement les 18-25 ans.

### Cited Findings
**Bankin' (FR, depuis 2011)**
- La fiche App Store indique « Plus de 4 millions de personnes utilisent déjà Bankin' en Europe ». Abonnements in-app sur la fiche US : Bankin' Plus annuel à 35,99 US$, Bankin' Plus+ annuel à 34,99 US$. — [App Store](https://apps.apple.com/us/app/bankin-g%C3%A9rer-son-budget/id447040033?l=fr-FR)
- Les chiffres d'utilisateurs se contredisent selon les sources : « plus de 5,5 millions » (Empruntis, janvier 2023 **[ANCIEN]**), « plus de 6 millions » (description Trustpilot), « plus de 10 millions » (vidéo YouTube, non datée). Ce sont des chiffres déclaratifs et non audités. — [Empruntis](https://www.empruntis.com/rachat-credits/simulation-rachat-credits/reste-a-vivre/applications-gestion-budget/bankin-avis/) ; [Trustpilot](https://fr.trustpilot.com/review/www.bankin.com) ; [YouTube](https://www.youtube.com/watch?v=jHG7EqEX1jA)
- Google Play : note de 4,2 sur 61 675 avis. L'argumentaire met en avant « jusqu'à 350 € d'économies par an » et une épargne automatique. — [Google Play](https://play.google.com/store/apps/details?id=com.bankeen&hl=fr)
- Il existe une formule premium haut de gamme, Bankin' Pro, présentée à 8,33 €/mois (source tierce). — [Parrain du Web](https://parrainduweb.fr/blog/bankin-pro)
- Modèle B2B : l'API d'agrégation est commercialisée sous le nom « Bridge powered by Bankin' », avec par exemple un cas client Sage pour la récupération de flux bancaires et la comptabilité. — [Bridge](https://contact.bridgeapi.io/case-study-sage)
- Rentabilité : un post LinkedIn d'un investisseur (décembre 2025) affirme qu'en 2025 « Bankin' dépasse les 40 % » de la Rule of 40. Seul l'extrait est disponible, la page n'a pas pu être lue. — [LinkedIn G. Sarthoulet](https://fr.linkedin.com/posts/guillaume-sarthoulet-800a0b2_la-rule-of-40-vous-connaissez-bankin-activity-7407818362652676097-N-OO)

**Linxo (FR, depuis 2010) — [RACHAT] par le Crédit Agricole**
- Chronologie officielle : création en 2010, première appli PFM en France en 2011, agrément d'établissement de paiement (entité Oxlin) en 2018, **Crédit Agricole actionnaire majoritaire en 2020**, Oxlin rebaptisé Linxo Connect en 2022, nouveau CEO en 2024, **nouvelle application et marque unifiée Linxo en 2025**. — [Linxo, Qui sommes-nous (mis à jour en juillet 2026)](https://linxo.com/qui-sommes-nous/)
- Modèle mixte : une appli B2C gratuite avec des offres Premium, et une activité B2B d'open banking (AISP, PISP, enrichissement de données via API) vendue aux banques, fintechs, entreprises et gestionnaires de patrimoine. Plus de 1 700 établissements financiers sont connectés. Le nombre d'utilisateurs n'est pas communiqué. — [Linxo](https://linxo.com/qui-sommes-nous/)
- Contradiction sur le prix : Selectra écrit que la nouvelle application « Linxo Lab » est « entièrement gratuite », alors que le site Linxo mentionne des offres Premium. — [Selectra](https://selectra.info/finance/guides/compte-bancaire/linxo)
- Partenariat de distribution avec BforBank, banque en ligne du groupe Crédit Agricole. — [Crédit Agricole](https://www.credit-agricole.com/communiques-de-presse-generaux/communique-de-presse-bforbank-linxo-et-bforbank-s-associent-pour-apporter-de-nouvelles-solutions-dans-la-gestion-bancaire)

**Finary (FR, suivi de patrimoine, pivot vers l'investissement)**
- **Série B de 25 M€ le 18/09/2025**, menée par PayPal Ventures avec LocalGlobe, Hedosophia, Shapers, Y Combinator et Speedinvest. À cette date, Finary revendique plus de 600 000 utilisateurs et une **rentabilité atteinte au T4 2024**. — [Finary, annonce de la série B](https://finary.com/en/product-updates/finary-series-b-raises-25m) ; [Maddyness](https://www.maddyness.com/2025/09/18/la-fintech-finary-leve-25-millions-deuros-avec-paypal-et-y-combinator/)
- La page d'accueil actuelle affiche « + d'1M d'utilisateurs » et « Démarrer gratuitement ». — [finary.com/fr](https://finary.com/fr)
- Produits : agrégation et suivi du patrimoine net, budget, compte-titres et PEA, PER, offre de gestion de patrimoine « Finary One ». Côté IA, Finary annonce un « AI agent » chargé de guider l'utilisateur vers ses objectifs, avec des insights IA et une gestion de l'argent « entièrement automatisée et personnalisée ». Expansion prévue vers d'autres marchés européens. — [Finary](https://finary.com/en/product-updates/finary-series-b-raises-25m)

**Powens (ex-Budget Insight, FR) — B2B pur**
- Budget Insight est devenu Powens en octobre 2022 **[ANCIEN]**. Son API unifiée couvre les comptes, l'épargne, les crédits, l'investissement et la crypto, avec plus de 1 800 banques européennes connectées. Les offres sont destinées aux banques, aux fintechs et aux gestionnaires de patrimoine. — [BusinessWire 2022](https://www.businesswire.com/news/home/20221024005035/en/Budget-Insight-Becomes-Powens-and-Accelerates-Its-European-Roadmap) ; [Powens, agrégation](https://www.powens.com/products/financial-data-aggregation/)
- Une release produit au T1 2025 a apporté des évolutions à l'agrégation, à la data insight et au paiement. — [Powens](https://www.powens.com/blog/winter-2025-product-news/)

**Tink (UE) — B2B**
- Le module « Money Manager » fournit en marque blanche aux banques des outils PFM : budgets, objectifs d'épargne, notifications personnalisées. — [Tink](https://tink.com/products/money-manager/)

### Inferences
- Le modèle économique dominant combine un **freemium B2C** (premium autour de 3 à 8 €/mois) et une **monétisation B2B de l'infrastructure** (Bridge, Linxo Connect, Powens). L'appli grand public sert de vitrine et de source de volume, et la marge se fait sur l'API. Pour Racines, l'agrégation n'est donc pas un différenciateur en soi : c'est une commodité qu'on achète à Powens, Bridge, Linxo Connect ou Tink.
- La consolidation est nette : Linxo a été absorbé par une banque, Budget Insight est devenu une infra B2B, et Finary a pivoté de l'agrégation vers l'investissement. L'agrégation pure en B2C se monétise mal.
- Tous ces acteurs ciblent des adultes déjà bancarisés, et souvent aisés dans le cas de Finary. **Aucun ne s'adresse explicitement aux 18-25 ans ni ne propose de dimension familiale ou intergénérationnelle.**

### Gaps
- Bankin' : aucun chiffre d'utilisateurs actifs ni de CA 2025 n'a été trouvé dans une source primaire, et les chiffres déclarés vont de 4 à 10 M. Aucune fonctionnalité IA (assistant, coach) n'a été trouvée dans les sources consultées : à vérifier directement dans l'appli.
- Linxo : nombre d'utilisateurs et prix exact du Premium en 2026 introuvables.
- Finary : nombre d'abonnés payants, prix de Finary Plus et date de lancement effective de l'agent IA introuvables.
- **Moneytrackin** : aucune source trouvée. Statut inconnu, l'outil est peut-être inactif.
- Tink : propriété actuelle (rachat par Visa) et volumes non vérifiés dans cette session.

---

## Q2. Néobanques jeunes et famille en France/UE : âges, fonctions parentales, prix, utilisateurs, statut en 2026

### Takeaway
Le segment des ados en France s'est **fortement contracté**. **Kard** a été liquidé (septembre 2025, 200 000 clients, fermeture définitive le 11/01/2026) et **Vybe** a fermé. Le statut de **Xaalys** est incertain : MoneyVox le classe parmi les applis « disparues ». **Pixpay** est le leader survivant : environ 600 k utilisateurs actifs, 240 k abonnés payants, plus de 10 M€ d'ARR, rentabilité visée fin 2025, groupe Acorns. Il intègre un « coach budgétaire intelligent ». Ces offres **s'arrêtent à 18 ans**. Pour les 18-25 ans, ce sont les banques traditionnelles qui contre-attaquent avec des forfaits à environ 3 €/mois.

### Cited Findings
**Pixpay (FR, lancé en 2019) — actif — [RACHAT] groupe GoHenry puis Acorns**
- Accessible dès 8 ans, de 3,99 € à 9,99 €/mois en juin 2026. Contrôle parental très complet : blocage par catégorie, plafonds, notification à chaque achat, recharge instantanée par CB, blocage de la carte. Volet éducatif : missions rémunérées et budget. — [Banqcompare (mis à jour le 11/06/2026)](https://banqcompare.com/comparer-les-banques/par-profil/comptes-bancaires-adolescents.html)
- Chiffres de juin 2025 : **plus de 10 M€ d'ARR**, **240 000 abonnés payants** pour une base active de **près de 600 000 utilisateurs**, CA en hausse de 55 % en 2024, rentabilité visée fin 2025. Trois formules à l'époque : 2,99, 5,99 et 9,99 €/mois. **« Coach budgétaire intelligent » déployé au S1 2025** dans le cadre d'une refonte de l'appli. Rapprochement avec GoHenry en juin 2022, puis avec Acorns en avril 2023. Le groupe Acorns revendique plus de 6 M d'utilisateurs. — [Croissance Investissement (19/06/2025)](https://croissanceinvestissement.com/pixpay-a-depasse-la-barre-des-10-millions-deuros-darr-et-atteindra-la-rentabilite-fin-2025/)
- Le prix d'entrée est passé de 2,99 € (2025) à 3,99 € (2026), ce qui suggère une hausse tarifaire. — [Banqcompare](https://banqcompare.com/comparer-les-banques/par-profil/comptes-bancaires-adolescents.html) vs [Croissance Investissement](https://croissanceinvestissement.com/pixpay-a-depasse-la-barre-des-10-millions-deuros-darr-et-atteindra-la-rentabilite-fin-2025/)
- Levées de fonds : 3,1 M€ en 2019, 8 M€ en 2020 (Global Founders Capital et Bpifrance), puis « 55 M$ en 2022 (avec GoHenry) » **[ANCIEN]**. — [Welcome to the Jungle](https://www.welcometothejungle.com/fr/companies/pixpay-1/culture-1) ; [Bpifrance](https://presse.bpifrance.fr/pixpay-accelere-son-developpement-et-annonce-une-levee-de-fonds-de-8-millions-deuros-aupres-de-global-founders-capital-et-de-bpifrance)
- Le baromètre annuel Pixpay de septembre 2026 donne 27 € d'argent de poche moyen par mois, et 64 % des ados en mettent une partie de côté. — [Le Figaro (01/09/2026)](https://www.lefigaro.fr/conjoncture/ils-sont-de-plus-en-plus-responsables-64-des-ados-mettent-une-partie-de-leur-argent-de-poche-de-cote-selon-une-etude-20260901) ; [Le Parisien (04/09/2026)](https://www.leparisien.fr/economie/votre-argent/on-apprend-a-tenir-un-budget-pour-leur-argent-de-poche-les-ados-preferent-la-carte-bancaire-au-liquide-04-09-2026-Z5IQBUKXJNAFNG54QGONQHDO7U.php)
- Partenariat avec 11 marques populaires auprès de la génération Z (date non précisée). — [Orange Actu](https://actu.orange.fr/videos/economie/start-up-co-la-banque-des-adolescents-pixpay-s-associe-avec-11-marques-phares-de-la-generation-z-17-06-CNT000002t6fs9.html)

**Kard (FR, 10-18 ans) — [FERMÉ]**
- Liquidation judiciaire prononcée le 11 septembre 2025 par le tribunal de commerce d'Évreux. Elle touche **200 000 utilisateurs**, pour **plus de 15 M€ levés** au total. Cause principale avancée : en avril 2025, Okali, prestataire technique de la chaîne de paiement, aurait résilié son contrat. Les Échos citent aussi les difficultés propres au segment ado : peu de transactions, forte pression sur les prix, contrôles renforcés sur les mineurs. — [Les Échos (25/11/2025)](https://www.lesechos.fr/finance-marches/banque-assurances/ce-netait-pas-complique-dappeler-la-faillite-de-kard-la-neobanque-des-ados-plonge-200000-clients-dans-lincertitude-2200696)
- Kard avait été « repris il y a un an » (vers 2024). Les clients avaient jusqu'au 11 novembre 2025 pour récupérer leurs fonds. — [MoneyVox (26/09/2025)](https://www.moneyvox.fr/banque-en-ligne/actualites/105244/cette-neobanque-pour-les-jeunes-risque-de-mettre-la-cle-sous-la-porte)
- Application définitivement fermée le 11 janvier 2026. — [Connect Banque](https://www.connectbanque.com/fr/actualites/fermeture-definitive-de-kard-que-faire-les-alternatives)
- Avant sa fermeture : dès 10 ans, 2,99 €/mois, cagnottes et virements entre amis. — [Banqcompare](https://banqcompare.com/comparer-les-banques/par-profil/comptes-bancaires-adolescents.html)

**Vybe (FR, 13-17 ans) — [FERMÉ]**
- Placée en liquidation judiciaire « à la mi-juillet », avec 40 000 utilisateurs. L'année exacte n'apparaît pas dans l'extrait (probablement 2022 **[ANCIEN]**). Vybe avait levé 2,2 M€ pour se lancer en septembre 2020. — [Les Échos](https://www.lesechos.fr/start-up/ecosysteme/la-neobanque-vybe-cesse-son-activite-1779203) ; [FrenchWeb](https://www.frenchweb.fr/vybe-leve-22-millions-deuros-pour-lancer-sa-neobanque-pour-ados/402481) ; [NeoBanques.app : « Fermé »](https://neobanques.app/vybe.htm)

**Xaalys (FR, 12-17 ans) — statut incertain**
- Dernière fiche disponible, du 01/04/2024 **[ANCIEN]** : offre gratuite et Premium à partir de 2,99 €/mois (4,99 € pour 2 enfants, 6,99 € pour 3), appli miroir parent-ado, cagnottes, coffre-fort, jeux et quiz éducatifs, distribution automatique de l'argent de poche. — [Comparabanques](https://www.comparabanques.fr/xaalys)
- En septembre 2025, MoneyVox écrit « Après Vybe et Xaalys, c'est une nouvelle application […] qui risque de disparaître », ce qui laisse entendre que Xaalys a cessé son activité. La date et les causes ne sont pas précisées. — [MoneyVox](https://www.moneyvox.fr/banque-en-ligne/actualites/105244/cette-neobanque-pour-les-jeunes-risque-de-mettre-la-cle-sous-la-porte)

**Revolut <18 (UE)**
- Accessible dès 6 ans et gratuit avec l'offre Standard, relié au compte du parent. Contrôle parental « basique », objectifs d'épargne visuels. — [Banqcompare (06/2026)](https://banqcompare.com/comparer-les-banques/par-profil/comptes-bancaires-adolescents.html)
- Revolut revendique plus de 70 M de clients dans le monde (avril 2026). — [FinTech Weekly](https://www.fintechweekly.com/news/revolut-air-ai-assistant-uk-customers-launch-2026)

**Sumeria (ex-Lydia, FR)**
- Sumeria regroupe les services bancaires historiques de Lydia. Son propre blog note que « seules certaines banques proposent des cartes à destination des 12-17 ans ». — [Sumeria, blog](https://sumeria.eu/blog/budget/argent-de-poche-comment-eviter-les-derives-de-ses-enfants-etudiants/)
- **Frais d'inactivité de 3 €/mois à partir du 12 mars 2026.** Formules payantes à partir de 4,99 €/mois avec un engagement de 6 mois. — [France Transactions (28/02/2026)](https://www.francetransactions.com/actus/news-banques/sumeria-ex-lydia-frais-inactivite-compte.html) ; [MoneyVox](https://www.moneyvox.fr/banque-en-ligne/sumeria)

**Nickel (FR)**
- Compte jeune à 20 €/an (date de la source non précisée). — [Selectra](https://selectra.info/finance/actualites/banque/offres-neobanques-adolescent)

**Banques traditionnelles : offres 18-25 ans (2026)**
- Crédit Agricole : 18-25 ans, à partir de 3 €/mois carte incluse. BNP Paribas : 18-24 ans, un an de gratuité sur certains services et jusqu'à 175 € d'avantages. SG : 18-24 ans, offre « Sobrio » à partir de 3 €/mois avec carte Visa Evolution. La Banque Postale : « Pass Jeune », avec cartes personnalisées et cadeaux. Les remises annoncées vont de 50 à 85 %, pour un coût moyen d'environ 34 €/an chez les 18-25 ans au 1er avril 2026. Aucune fonction de budget, d'éducation ou d'IA n'est mentionnée. — [Meilleurtaux (03/05/2026)](https://banque.meilleurtaux.com/banque-en-ligne/actualites/2026-avril/banques-traditionnelles-la-riposte-pour-les-18-30-ans.html)
- L'offre Jeune BNP comprend un compte courant gratuit, une carte Mastercard gratuite et un découvert négociable de 500 à 1 000 €. — [Bourse des crédits (19/10/2026)](https://www.boursedescredits.com/guide-bnp-paribas-avis-clients-experts-2026-6372.php)
- SG accorde aussi 20 % de remise aux 25-29 ans. — [SG](https://particuliers.sg.fr/ouvrir-compte-bancaire-en-ligne/ouverture-compte-jeunes)

### Inferences
- Le segment des **mineurs** est économiquement fragile : peu de transactions, prix bas, conformité lourde. Trois acteurs français sur quatre de la vague 2019-2020 (Kard, Vybe et probablement Xaalys) ont disparu. Seul Pixpay survit, adossé à un groupe international et à un modèle d'abonnement.
- **Leçon pour Racines** : Kard est tombé à cause d'une dépendance à un prestataire de paiement (Okali). Un compte de paiement opéré en BaaS crée un risque de concentration sur le partenaire, qu'il faut traiter dans le business plan (double fournisseur, choix d'un établissement agréé solide).
- **Trou de marché à 18 ans** : les néobanques ados s'arrêtent à la majorité, et les banques traditionnelles captent les 18-25 ans par le prix (environ 3 €/mois) sans aucun outil pédagogique. La transition « ado vers jeune adulte » n'est couverte par aucun acteur spécialisé en France.

### Gaps
- Statut 2026 de Xaalys non confirmé par une source primaire (annonce de fermeture ou de rachat introuvable).
- N26 : aucune offre jeunesse trouvée dans les sources consultées.
- Revolut : pas de chiffre d'utilisateurs <18 ni de détail sur une offre spécifique 18-24 ans.
- Sumeria et Nickel : nombre d'utilisateurs jeunes non trouvé. Possibilité pour des proches de verser de l'argent : non documentée hors fonction P2P générique.

---

## Q3. Références US/UK (Greenlight, GoHenry/Acorns Early, Step, Copper, Rooster Money) : financement familial, éducation, prix

### Takeaway
Les références anglo-saxonnes sont plus matures que les françaises sur la **dimension famille élargie**. Acorns Early (ex-GoHenry) propose des **Giftlinks** et des **comptes « Relatives »** qui permettent aux proches d'envoyer de l'argent. Rooster Money est intégré à NatWest, et Greenlight propose des jeux éducatifs et une distribution en marque blanche via les banques. Le prix tourne autour de 6 à 20 $/mois par famille. Ici aussi, ces offres **visent les 6-18 ans** et non les jeunes adultes. Copper a fermé ses services bancaires en 2024 après la faillite de Synapse.

### Cited Findings
**Greenlight (US)**
- De 5,99 à 19,98 $/mois pour jusqu'à 5 enfants, prix par famille. Greenlight Max (10,98 $/mois) ajoute l'investissement pour les enfants et 1 % de cashback. — [Acorns, comparatif](https://www.acorns.com/learn/acorns/acorns-early-vs-greenlight/)
- « Greenlight Level Up » est un jeu d'éducation financière intégré à l'appli. Le modèle est **B2B2C** : distribution via des banques et credit unions (partenariat Alkami, United Community, Torrington Savings Bank, février 2025). — [United Community](https://ir.ucbi.com/news-releases/news-release-details/united-community-partners-greenlight-help-families-raise) ; [Alkami](https://www.alkami.com/news/alkami-and-greenlight-partner-to-bring-youth-banking-to-financial-services/) ; [RBJ (02/2025)](https://rbj.net/2025/02/07/community-banks-new-partnership-emphasizes-financial-literacy-for-children-and-teens/)
- Fonctions : tâches ménagères rémunérées, argent de poche automatique, objectifs d'épargne, suivi des dépenses par le parent. — [App Store Greenlight](https://apps.apple.com/us/app/greenlight-for-families/id1049340702)

**Acorns Early (ex-GoHenry, US/UK) — [RACHAT]**
- 8 $/mois pour Acorns Early Lite, sans investissement pour l'enfant, ou inclus dans Acorns Gold à 12 $/mois, qui ajoute l'investissement. — [Acorns](https://www.acorns.com/learn/acorns/acorns-early-vs-greenlight/) ; [Penny Time (2026)](https://www.pennytime.app/learn/blog/cash-app-for-kids-vs-greenlight-vs-acorns-early-h/)
- Contradiction : Finder évoque des formules Basic à 8 $ et Family à 10 $/mois, sans doute une grille antérieure. — [Finder](https://www.finder.com/kids-banking/gohenry-vs-greenlight)
- **Financement par les proches** : la page support GoHenry décrit les « Giftlinks, when friends and family send money to your kid's card » et les « Relatives, when family members use their Relatives account ». La page renvoie aujourd'hui une erreur 404 après redirection vers support.acorns.com ; seul l'extrait du moteur de recherche est disponible. — [GoHenry, support (extrait)](https://us.support.gohenry.com/us/s/article/What-s-changing-now-that-GoHenry-is-becoming-Acorns-Early)

**NatWest Rooster Money (UK)**
- Carte prépayée et appli d'argent de poche pour les 6-17 ans, avec tableau d'étoiles (« Star Chart »), suivi de l'argent virtuel, tâches et objectifs d'épargne. Gratuit pour les clients NatWest, sinon 1,99 £/mois ou 19,99 £/an. — [NatWest](https://www.natwest.com/current-accounts/childrens-accounts/debit-card-under-18s.html) ; [NatWest, aide](https://www.natwest.com/support-centre/help-with-your-product/rooster-money/what-is-natwest-rooster-money.html)
- Trustpilot : 4,7 sur 3 106 avis. Les utilisateurs citent la gestion de l'« argent offert » (gifted money). — [Trustpilot](https://nz.trustpilot.com/review/www.roostermoney.com)
- Toujours actif en juin 2026 (communiqué NatWest Group). — [NatWest Group (06/2026)](https://www.natwestgroup.com/news-and-insights/news-room/press-releases/financial-capability-and-learning/2026/jun/mow-money-no-problems-great-out-chores-boost-kids-pay-packets-ac.html)

**Copper (US) — [FERMÉ] (services bancaires)**
- En mai 2024, Copper a dû arrêter brutalement ses comptes et ses cartes de débit après la mise à l'arrêt de son prestataire BaaS Synapse. — [TechCrunch (21/05/2024)](https://techcrunch.com/2024/05/21/teen-fintech-copper-had-to-emergency-discontinue-its-banking-debit-products/) ; [Banking Dive](https://www.bankingdive.com/news/fintech-copper-burned-by-synapse-collapse/717407/)
- En 2022, Copper comptait près de 1 M d'utilisateurs et avait levé 29 M$ **[ANCIEN]**. — [GeekWire](https://www.geekwire.com/2022/copper-a-banking-app-for-teens-with-nearly-1m-users-lands-29m-to-expand-into-investing/)

### Inferences
- Le schéma Giftlinks/Relatives d'Acorns Early est **la référence la plus proche de la brique « argent des proches » de Racines**. Il reste centré sur l'argent de poche des enfants, sans fléchage par projet ni carte cadeau « engagée ».
- Copper et Kard ont connu le même scénario : le **risque BaaS**, c'est-à-dire la dépendance à un intermédiaire technique, est un risque systémique sur ce segment, des deux côtés de l'Atlantique.
- Le modèle B2B2C de Greenlight via les banques est une piste de distribution transposable en France (marque blanche pour les réseaux bancaires).

### Gaps
- **Step (US)** : aucune information à jour trouvée dans les sources consultées (statut, prix, utilisateurs).
- Greenlight : nombre d'utilisateurs et derniers financements non trouvés. Fonctions d'IA non documentées (un avis App Store parle d'« ai » pour l'automatisation des virements, ce qui n'est pas fiable).
- Acorns Early : présence UK actuelle et prix au Royaume-Uni non confirmés, la page support est en 404.

---

## Q4. Qui intègre déjà de l'IA (assistant, coach budget, catégorisation) en 2025-2026 ?

### Takeaway
L'IA conversationnelle financière est en train de devenir standard chez les **grands acteurs et les spécialistes US**. **Revolut AIR** a été lancé au Royaume-Uni le 9 avril 2026. **Cleo** revendique plus de 250 M$ d'ARR et plus de 1 M d'abonnés payants en 2025. Finary annonce un « agent IA » et Pixpay un « coach budgétaire intelligent » (S1 2025). En France, **aucun acteur n'associe un coach IA pédagogique à une cible 18-25 ans et à la famille**.

### Cited Findings
- **Revolut AIR (« AI by Revolut »)** : déploiement auprès des 13 M de clients britanniques à partir du **9 avril 2026**. Interface conversationnelle unique qui couvre l'analyse des dépenses, le suivi des investissements, la gestion des abonnements, le gel de carte et le voyage (eSIM). Politique de **conservation zéro des données** chez les fournisseurs IA tiers, validation biométrique pour les actions sensibles. **Aucun calendrier n'est annoncé pour les autres marchés**, la France n'est donc pas couverte à cette date. — [FinTech Weekly (11/04/2026)](https://www.fintechweekly.com/news/revolut-air-ai-assistant-uk-customers-launch-2026) ; [Revolut AIR](https://www.revolut.com/air-ai-by-revolut/)
- Revolut avait annoncé cet assistant IA dans sa feuille de route 2025. — [Revolut](https://www.revolut.com/en-HR/news/revolut_reveals_2025_vision_with_ai_assistant_mortgages_and_atms_on_the_horizon/)
- **Cleo (UK/US)** : « AI money coach » qui parle, raisonne et se souvient (voix et mémoire, juillet 2025). En 2025, Cleo est en passe de dépasser **1 M d'abonnés payants**, avec plus de **250 M$ d'ARR** (plus de 2x sur un an) et une rentabilité nette. — [BusinessWire (29/07/2025)](https://www.businesswire.com/news/home/20250729690058/en/Cleo-Becomes-the-First-AI-Money-Coach-That-Speaks-Thinks-and-Remembers)
- Cleo revendique plus de 9 M d'utilisateurs (Google Play : 4,6 sur 155 475 avis). Le modèle mêle avances de trésorerie, crédit et abonnements. — [Google Play](https://play.google.com/store/apps/details?id=com.meetcleo.cleo&hl=en_US)
- Cleo aurait versé 17 M$ pour régler un litige avec la FTC américaine (information relayée par un post Facebook de Fox59, source secondaire à vérifier). — [Fox59 / Facebook](https://www.facebook.com/Fox59News/posts/if-youve-used-the-ai-based-cash-advance-app-cleo-you-may-be-receiving-a-payment-/1713206570405736/)
- **Finary** : « AI agent » pour guider proactivement vers les objectifs et automatiser la gestion de l'argent (annonce de septembre 2025). — [Finary](https://finary.com/en/product-updates/finary-series-b-raises-25m)
- **Pixpay** : « coach budgétaire intelligent » déployé au S1 2025. — [Croissance Investissement](https://croissanceinvestissement.com/pixpay-a-depasse-la-barre-des-10-millions-deuros-darr-et-atteindra-la-rentabilite-fin-2025/)
- **Tink** : notifications personnalisées et PFM en marque blanche pour les banques (pas d'IA générative mentionnée). — [Tink](https://tink.com/products/money-manager/)

### Inferences
- Le positionnement « coach IA » seul n'est **plus différenciant en 2026** : Revolut, Cleo, Finary et Pixpay l'ont ou l'annoncent. La différenciation possible tient au **contenu pédagogique** (et non au simple chatbot transactionnel), à la **cible 18-25 ans en France** et au **contexte familial**, par exemple un coach qui explique l'usage des fonds reçus des proches.
- Cleo montre le risque réglementaire et réputationnel d'un coach IA monétisé par le crédit (litige FTC). Une approche éducative, sans incitation au crédit, est un argument de positionnement.
- Revolut AIR applique une conservation zéro des données et une validation biométrique : c'est un standard de conformité à reprendre.

### Gaps
- Bankin', Linxo, Lydia/Sumeria : aucune fonctionnalité IA générative documentée dans les sources consultées (ce qui ne prouve pas qu'elle n'existe pas).
- Revolut AIR : prix (gratuit ou réservé à certains plans) et disponibilité pour les comptes <18 non trouvés.
- Contenu réel du « coach » Pixpay (IA générative ou règles) non détaillé.

---

## Q5. Qui permet aux proches et grands-parents d'envoyer de l'argent et de suivre la progression ? Où est l'espace vacant ?

### Takeaway
Seuls **Acorns Early (Giftlinks et comptes Relatives)** et, dans une moindre mesure, **Rooster Money** (« gifted money ») formalisent l'envoi d'argent par la famille élargie, et uniquement pour des **enfants de 6 à 18 ans** au US/UK. En France, Pixpay et les néobanques ados se concentrent sur la relation **parent-enfant**. **Aucun acteur identifié ne combine agrégation de comptes, compte de paiement alimenté par les proches, cartes cadeaux « engagées » (fléchées vers un projet) et coach IA pédagogique pour les 18-25 ans.** C'est l'espace vacant de Racines.

### Cited Findings
- Acorns Early : « Giftlinks, when friends and family send money to your kid's card ; Relatives, when family members use their Relatives account ». — [GoHenry, support (extrait)](https://us.support.gohenry.com/us/s/article/What-s-changing-now-that-GoHenry-is-becoming-Acorns-Early)
- Rooster Money : les utilisateurs citent la gestion de l'argent de poche et de l'« argent offert ». — [Trustpilot](https://nz.trustpilot.com/review/www.roostermoney.com)
- Pixpay : les parents ou tuteurs peuvent verser de l'argent depuis leur compte. Aucune fonction « grands-parents » documentée. — [Paris Match](https://www.parismatch.com/Guide-shopping/carte-bancaire-pour-mineur-laquelle-choisir-pour-une-gestion-simplifiee-260087) ; [Croissance Investissement](https://croissanceinvestissement.com/pixpay-a-depasse-la-barre-des-10-millions-deuros-darr-et-atteindra-la-rentabilite-fin-2025/)
- Kard (fermé) proposait des cagnottes et des virements entre amis. — [Banqcompare](https://banqcompare.com/comparer-les-banques/par-profil/comptes-bancaires-adolescents.html)
- Les cagnottes de projet existaient en 2019-2020 chez Orange Bank, Pixpay, Revolut Junior et Xaalys **[ANCIEN]**. — [Mind Fintech](https://www.mind.eu.com/fintech/article/neobanques-pour-ados-plus-doffres-mais-encore-peu-de-clients/)

### Tableau comparatif (état au 30/10/2026)

| Acteur | Pays | Statut 2026 | Cible / âges | Offre clé | Prix | Modèle économique | Utilisateurs (source, date) | Financement | IA | Argent des proches | Agrégation |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **Bankin'** | FR | Actif | Adultes | PFM, budget, épargne auto | Freemium. Plus ~35 US$/an (App Store), Pro ~8,33 €/mois | Premium B2C + API B2B Bridge | 4 M+ (App Store, non daté) ; 6 à 10 M déclarés selon les sources | Inconnu | Non documentée | Non | **Oui** |
| **Linxo** | FR | Actif, **filiale Crédit Agricole** depuis 2020 | Adultes | PFM, nouvelle appli 2025 | Gratuit + Premium (contradiction Selectra) | B2C + open banking B2B (Linxo Connect) | Inconnu | Groupe CA | Non documentée | Non | **Oui** |
| **Finary** | FR | Actif, pivot vers l'investissement | Adultes épargnants | Patrimoine, PEA, PER, CTO, Finary One | Freemium (Plus : prix inconnu) | Abonnements + courtage + gestion de patrimoine | 600 k+ (09/2025) ; 1 M+ (site 2026) | Série B 25 M€ (09/2025, PayPal Ventures) ; rentable au T4 2024 | **Agent IA annoncé** | Non | **Oui** |
| **Powens** (ex-Budget Insight) | FR | Actif, B2B | Entreprises | API d'agrégation, 1 800+ banques | B2B | API | n/a | Inconnu | n/a | n/a | Brique technique |
| **Tink** | UE | Actif, B2B | Banques | API + Money Manager (PFM marque blanche) | B2B | API | n/a | Inconnu | Notifications personnalisées | n/a | Brique technique |
| **Moneytrackin** | — | **Inconnu** | — | — | — | — | — | — | — | — | — |
| **Pixpay** | FR | Actif, groupe Acorns | 8-18 ans + parents | Carte, appli miroir, missions, épargne | 3,99 à 9,99 €/mois (2026) | Abonnement | ~600 k actifs, 240 k payants (06/2025) | 3,1 M€ (2019), 8 M€ (2020), 55 M$ avec GoHenry (2022) | **Coach budgétaire intelligent (S1 2025)** | Parents uniquement (documenté) | Non |
| **Kard** | FR | **[FERMÉ]** liquidation 09/2025, appli fermée le 11/01/2026 | 10-18 ans | Carte, cagnottes | 2,99 €/mois | Abonnement | 200 k (11/2025) | 15 M€+ | Non | Virements entre amis | Non |
| **Xaalys** | FR | **Incertain**, probablement fermé | 12-17 ans | Carte, quiz éducatifs | Gratuit / 2,99 €+ (2024) | Abonnement | Inconnu | Inconnu | Non | Parents | Non |
| **Vybe** | FR | **[FERMÉ]** | 13-17 ans | Carte | — | — | 40 k | 2,2 M€ (2020) | Non | — | Non |
| **Revolut <18** | UE | Actif | 6-17 ans (lié au parent) | Carte, objectifs d'épargne | Gratuit (Standard) | Interchange + plans payants du parent | 70 M+ clients Revolut au total (04/2026) | — | **AIR (UK seulement, 04/2026)** | Parent | Non (pas pour <18) |
| **Sumeria** (ex-Lydia) | FR | Actif | Jeunes adultes / tous | Compte, carte, P2P | À partir de 4,99 €/mois ; frais d'inactivité 3 €/mois (03/2026) | Abonnements + frais | Inconnu | Inconnu | Non documentée | P2P générique | Non |
| **Nickel** | FR | Actif | Tous, compte jeune | Compte en buraliste | 20 €/an (jeune) | Frais | Inconnu | Groupe BNP (non vérifié ici) | Non documentée | Non | Non |
| **Banques (CA, BNP, SG, LBP)** | FR | Actif | 18-24/25 ans | Forfait jeune | ~3 €/mois, ~34 €/an en moyenne (04/2026) | Acquisition long terme | — | — | Non mentionnée | Non | Non |
| **Greenlight** | US | Actif | Enfants et ados | Carte, tâches, Level Up, investissement | 5,99 à 19,98 $/mois par famille | Abonnement + B2B2C bancaire | Inconnu | Inconnu | Non documentée | Parents | Non |
| **Acorns Early** (ex-GoHenry) | US/UK | Actif, **[RACHAT]** | 6-18 ans | Carte, éducation, investissement (Gold) | 8 $/mois (Lite), 12 $/mois (Gold) | Abonnement | Groupe Acorns 6 M+ (2025) | — | Non documentée | **Oui : Giftlinks + comptes Relatives** | Non |
| **Rooster Money** (NatWest) | UK | Actif | 6-17 ans | Carte prépayée, Star Chart, tâches | 1,99 £/mois (gratuit pour les clients NatWest) | Rétention bancaire | Inconnu | NatWest | Non documentée | « Gifted money » (avis) | Non |
| **Copper** | US | **[FERMÉ]** banque en 05/2024 (Synapse) | Ados | Banque + investissement | — | — | ~1 M (2022) | 29 M$ (2022) | — | — | Non |
| **Step** | US | **Inconnu** | Ados | — | — | — | — | — | — | — | — |
| **Cleo** | UK/US | Actif | Jeunes adultes (Gen Z) | Coach IA, avances, crédit | Abonnements | Abonnements + avances | 9 M+ (Google Play) ; 1 M+ payants (2025) | Inconnu | **Coach IA voix + mémoire** | Non | Oui (lecture des comptes, US) |

### Inferences (white space pour Racines)
1. **Aucun acteur ne couvre les quatre briques** : agrégation, compte de paiement alimenté par les proches, cartes cadeaux engagées et coach IA éducatif. Les agrégateurs n'ont ni compte ni dimension familiale. Les néobanques ados n'agrègent rien et s'arrêtent à 18 ans. Les coachs IA (Cleo, Revolut AIR) ne gèrent ni la famille ni le don.
2. **La tranche 18-25 ans n'est pas servie** sur la pédagogie : les néobanques ados la perdent à la majorité, et les banques la captent par le prix (~3 €/mois) sans outil éducatif.
3. **Les grands-parents comme donateurs** ne sont adressés explicitement par aucun acteur français. La seule référence est Acorns Early (US/UK, Relatives et Giftlinks), limitée aux mineurs et sans fléchage de l'argent vers un projet.
4. Le **don « engagé »** (carte cadeau fléchée vers un projet, avec retour de progression au donateur) n'a pas d'équivalent trouvé chez les acteurs étudiés. Les cagnottes de projet existent mais sont alimentées par le jeune ou ses parents.
5. **Risques à intégrer** : l'économie unitaire du segment jeunes est fragile (Kard, Vybe, Copper), la dépendance BaaS a provoqué deux faillites, l'IA tend à se banaliser (Revolut AIR, Cleo, Pixpay, Finary), et la cible pourrait être reprise par Pixpay ou Acorns s'ils prolongent leur offre au-delà de 18 ans.

### Gaps
- Aucune vérification exhaustive des cartes cadeaux numériques (Wonderbox, cartes cadeaux bancaires, cagnottes type Leetchi ou Lydia) : hors périmètre de cette note, à croiser avec un autre volet de recherche.
- Absence de preuve n'est pas preuve d'absence : les fonctions « proches » de Pixpay, Revolut <18 et Sumeria n'ont pas été vérifiées directement dans les applis.
- Pas de données de téléchargements (Sensor Tower, data.ai) pour comparer les volumes.
