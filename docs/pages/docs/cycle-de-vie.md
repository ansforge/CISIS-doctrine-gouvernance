---
title: 🔁 Cycle de vie des spécifications
nav_order: 5
description: 
---

Il a été identifié qu'il n'est pas évident pour les développeurs de solutions d'identifier si la spécification est de qualité et de maturité suffisante pour pouvoir être implémentée en production sans craindre une évolution majeure dans un futur proche.
Il a donc été décidé de faire une tentative de mise en place de critères de qualité et de maturité accompagné de statuts associés à chaque spécification pour donner une idée à l'utilisateur de la qualité et de la maturité de la spécification.

Il est cependant important de noter que le statut de maturité n'est qu'une information, il est toujours préférable de se baser sur des spécifications qui ne sont pas très matures que sur une API à un format propriétaire, la transition vers la spécification mature sera toujours plus facile d'un format draft vers final que d'une spécification propriétaire vers une spécification standard.

## Le cycle de vie et les statuts associés

Quatre statuts ont été identifiées pour les spécifications d'interopérabilité de l'ANS : "draft" ou "brouillon", "public-comment" ou "en concertation", "trial-implementation" ou "pour implementation", et "final-text" ou "final".

Les statuts ont été inspirés des [pratiques d'IHE](https://wiki.ihe.net/index.php/Comments#Phases_of_Development) et adaptées pour les besoins nationaux. Il y a un label anglais pour correspondre aux statuts IHE ainsi que sa traduction française.
Les statuts "draft", "trial-implementation" et "final-text" reflètent la maturité des spécifications dans l'ordre indiqué.

### Le statut "draft" ou "brouillon"

Ce statut correspond à une spécification **en cours de développement**, il s'agit de son statut lors de la création de la spécification.
Le statut brouillon est particulièrement important pour les spécifications développées sur GitHub car tous les travaux sont publics et sont donc accessibles à tout moment : de la création du répertoire GitHub à la publication.

### Le statut "public comment" ou "en concertation"

La spécification est publiée **pour concertation publique**. La spécification en mode "public comment" risque d'évoluer suite aux commentaires des concertations et n'est pas faite pour être implémentatée : elle est en attente de la validation de l'écosystème pour publication.
Une spécification en « final-text » ou en «  trial-implementation » peut repasser en commentaire public en cas d'évolution majeure.

### Le statut "trial-implementation" ou "pour implémentation"

La spécification a passé une ou plusieurs phase de concertation et est **prête pour les premières implémentations** en situation réelle (projectathon, projet national …).
Ce statut est un reflet de la maturité : selon l'auteur, la spécification est prète pour une première implémentation.

### Le statut "final-text" ou "final"

Les auteurs de la spécification ont estimé qu'elle avait atteint le **stade de maturité le plus élevé**.
Ce stade est atteint lorsque la spécification a déjà été mise en œuvre dans un projet national ou testée lors d'un projectathon. La spécification a eu des retours post-concertation, post-projectathon ou post-implémentation et a été corrigée, indiquant un fort indice de confiance sur la maturité et la qualité de la spécification.
Ce statut est un reflet de la maturité : selon l'auteur, la spécification a déjà été éprouvée dans une ou plusieurs situations donnant un bon indice de confiance sur sa maturité. Ce statut indique aussi que les critères de maturité et de qualité définis ci-dessous ont été respectés.

### Les autres statuts

Une spécification peut également être "deprecated" ou "dépréciée" si celle-ci a été remplacée par une autre spécification ou "withdrawn" ou "retirée" après avoir été dépréciée depuis un moment.

### Le cycle de vie d'une spécification

Durant la vie d'une spécification, celle-ci passe par différents statuts exprimés dans le schéma ci-dessus.

![](../../assets/images/cycle-de-vie.png)

A noter, le statut de cycle de vie n'est pas associé à la version qui utilise le format semver.
Le numéro de version d'une spécification est systématiquement incrémenté à chaque release. Ce numéro de version est décorrélé du statut du cycle de vie. Par exemple, si une faute d'orthographe est corrigée et qu'il y a une incrémentation mineure du numéro de version, celle-ci ne justifie pas un changement de statut.
Lors de chaque nouvelle publication d'une spécification, le numéro de version va systématiquement être incrémenté. Le statut du cycle de vie va potentielleemnt évoluer en fonction du schéma ci-dessus.

Il est à noter qu'une version en final-text peut repasser en trial-use, par exemple dans le cas où il y a un changement majeur tel qu'un refactoring complet de la spécification (passage au format IG, à FHIR R6, ...). Ce cas signifie que l'ancienne version en final-text n'est plus à utiliser car la situation internationale nécessite ces évolutions.

Lorsqu'une nouvelle version d'une spécification est publiée, il est conseillé de la mettre en place au niveau des implémenteurs dans les 1 ou 2 ans à venir.

A l'issue d'une concertation, une spécification passer au statut « final-text ou « for implementation ». Ce choix dépend du respect de critère de qualité, de maturité, et du choix de l'auteur.
Pour passer en final-text, la spécification doit être passée par une implémentation nationale ou par des projectathons avec retours mineurs.

## Définition des critères de maturité

Le critère de maturité reflète la confiance de l’auteur de la spécification sur sa clarté et sa facilité d’implémentation. Une spécification avec un haut degré de maturité indique également une plus grande pérennité de la spécification. Il est cependant important de noter que la pérennité ne peut jamais être garantie, les spécifications jugées matures ont une plus forte probabilité que les évolutions soient rétro compatibles.

* Respect de l'ensemble des critères de qualité mentionnés ci-dessous
* (Etude en cours) Nombre d'implémentations obtenu par déclaration (par convergence ou par les DSI). Idéalement avec des retours d'expérience sur l'implémentation des spécifications
* Nombre de passage en projectathons, nombre de tests réalisés lors de projectathon, et nombre de partenaires
* Nombre d'issues et résolutions sur le repo GitHub
* Nombre de commentaires lors des phases de concertation

## Définition des critères de qualité

Les critères de qualité représentent un ensemble de règles à respecter pour être conforme aux attentes nationales, et ainsi proposer un format commun ainsi qu’un niveau de qualité constant sur l’ensemble de nos spécifications. Les critères de qualité sont propres à chaque standard.

Il n'est pas toujours possible de respecter strictement ces critères de qualité, notamment car l'écosystème national ne peut pas contrôler les spécifications internationales qui ne respectent pas forcément l'ensemble de ces critères, et d'autre part il y a des spécifications historiques qu'il n'est pas forcément possible de faire évoluer. L'objectif de ces critères est de les respecter et tendre le plus possible vers ceux-ci lorsque l'on fait évoluer des anciennes spécifications

Les critères de qualité **FHIR** sont :

* Respect des bonnes pratiques nationales tel que les règles de nommages indiquées ci-dessous
* Respect des [bonnes pratiques internationales](https://build.fhir.org/ig/FHIR/ig-guidance/best-practice.html)
* Respecter le stratégie nationale des choix de version FHIR
* Chaque ressource de conformité doit avoir une description
* L'ensemble des ressources de conformité doit avoir une description précise de son usage
* Publication de l'IG sans erreurs (cf session Q/A)
* Ne pas recréer des artifacts qui existent déjà au niveau national et international (nécessite de l'expertise, de la veille et de faire une analyse de l'existant international avant de débuter les travaux.)

Ces règles de nommage ont été établies en s'inspirant des ressources us-core

| **Paramètre** | **Objet concerné** | **Règle** | **Exemple us-core** |
| ----- | ----- | ----- | ----- |
| id | ressources de conformité | Utiliser le format kebab-case, ex : fr-core-patient.. Lors de la création d'un IG pour un projet en particulier, il est possible de préfixer l'ensemble des ressources de conformité par le trigramme du projet (ex : "ror-...") | us-core-patient |
| title | ressources de conformité | Similaire au nom, avec espaces. Ex : Fr Core Patient | US Core Patient Profile |
| name | ressources de conformité |  Utiliser le format PascalCase sans espace. Ex : FrCorePatient | USCorePatientProfile |
| url | ressources de conformité |  [base]/[ResourceType]/[id] (généré automatiquement par sushi). A noter que [ResourceType] doit respecter le nom et la casse des ressources définies dans FHIR core (ex: StructureDefinition). | http://hl7.org/fhir/us/core/StructureDefinition/us-core-patient |
| code  | SearchParameter|  Toujours en minuscule, mots séparés par des tirets "-" si besoin | gender-identity |
| name | slice | Utiliser l'id de l'extension s'il s'agit d'une extension sinon utiliser le format lowerCamelCase | us-core-genderIdentity |
| id | package | Utiliser des minuscules | hl7.fhir.us.core [lien vers la documentation](https://confluence.hl7.org/display/FHIR/NPM+Package+Specification) |

La documentation officielle se trouve sur le [confluence d'HL7](https://confluence.hl7.org/pages/viewpage.action?pageId=35718826#GuidetoDesigningResources-NamingRules&Guidelines)

Les critères de qualité **CDA** sont :

**A remplir par l'équipe CDA**

## Définition des métadonnées associées à une spécification d'interopérabilité

Les métadonnées correspondent aux données annexées aux spécifications. Elles sont utiles à des fins de recherche notamment.

| Nom | Description | Cardinalité | Exemples |
| --- | --- | --- | --- |
| identifiant | Identifiant ou URL identifiante d’accès à la spécification | 1..1 | https://interop.esante.gouv.fr/ig/fhir/pdsm |
| statut | Statut de la spécification selon les statuts définis par l’ANS. Les statuts peuvent être rédigés en anglais ou en français. | 1..1 | draft, public-comment, for-implementation, final-text |
| version | Version au format semver | 1..1 | 1.0.0 |
| code | Code qui définit la spécification | 1..1 | GAP, CR-BIO |
| titre | Titre de la spécification | 1..1 | Gestion d'Agendas Partagés |
| description | Description succinte du périmètre de la spécification | 1..1 | Ce guide d’implémentation a pour objet de permettre la gestion de ressources (personnes, lieux ou objets), la gestion des disponibilités de ces ressources, la consultation et la synchronisation d’agenda et la prise de rendez-vous. |
| date de dernière mise à jour | Date de dernière publication de la spécification | 1..1 | 2024-04-29 |
| Standards principaux | Standards syntaxiques et sémantiques, profils sur lesquels s'appuent la spécification | 0..* | CDA, FHIR, SNOMED CT |
| Contexte projet | Projet national ou référentiel notable où la spécification est utilisée | 0..1 | Mon Espace Santé |
| Catégorie | Catégorie métier de la spécification (équivalent des technical frameworks IHE) correspondant aux préfixes des spécifications CDA | 0..* | Liste des catégories : ANEST - Anesthésie, AVC - Accident vasculaire cérébral, BIO - Biologie, CANCER - Cancer, CARD - Cardiologie, IMG - Imagerie, OBP - Obstétrique et périnatalité, OPH - Ophtalmologie, TLM - Télémédecine, VAC - Vaccination (Demande d'ajout de nouvelles catégories : issues GitHub) |
| Type | Type de spécification | 0..* | Document médical, définition d'APIs, outillage, couche métier, couche service, couche transport, documentation, ... |
| Utilisations connues | Formulaire d’auto-déclaration de conformité pour les éditeurs (à définir) | 0..* | à définir |
| Porteur | Permet d’afficher le porteur de laspécification. Particulièrement important dans le cas de l’UP externe | 1..1 | ANS, InteropSanté |
| Contact | Permet d’afficher le contact de la spécification. Particulièrement important dans le cas de l’UP externe | 1..1 | ci-sis@esante.gouv.fr |
