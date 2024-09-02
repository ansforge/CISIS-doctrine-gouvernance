---
title: 🧭 Trajectoire interopérabilité
nav_order: 7
description: 
---

<div style="
    background-color: #fff5f5; 
    color: #e57373; 
    border: 1px solid #e57373; 
    padding: 10px; 
    border-radius: 5px; 
    font-size: 14px; 
    text-align: center; 
    max-width: 300px; 
    margin: 20px auto;
">
    ⚠️ Work in Progress
</div>


<!-- TOC generated with Auto Markdown TOC 
Nom : Auto Markdown TOC
ID : xavierguarch.auto-markdown-toc
Description : Markdown TOC (Table Of Contents) Plugin for Visual Studio Code.
Version : 2.1.4
Serveur de publication : Xavier Guarch
Lien de la Place de marché pour VS : https://marketplace.visualstudio.com/items?itemName=xavierguarch.auto-markdown-toc 
Transformé en HTML : https://markdowntohtml.com/ -->
<!-- TOC -->


<div class="wysiwyg">
    <ul>
        <li><a href="#quest-ce-que-linterop%C3%A9rabilit%C3%A9-">Qu&#39;est-ce que l&#39;interopérabilité ?</a></li>
        <li><a href="#strat%C3%A9gie-des-versions-fhir">Stratégie des versions FHIR</a>
            <ul>
                <li><a href="#nouveaux-cas-dusages-fhir-adress%C3%A9s-par-interopsant%C3%A9-et-lans--privil%C3%A9gier-fhir-r4-et-anticiper-la-transition-vers-r6">Nouveaux cas d’usages FHIR adressés par Interop’Santé et l’ANS : privilégier FHIR R4 et anticiper la transition vers R6</a></li>
                <li><a href="#ne-pas-cr%C3%A9er-dig-se-basant-sur-r5-sans-cas-dusage-identifi%C3%A9">Ne pas créer d’IG se basant sur R5 sans cas d’usage identifié</a></li>
                <li><a href="#priorit%C3%A9-fhir-france-en-2024-et-2025---am%C3%A9liorer-la-qualit%C3%A9-de-lexistant">Priorité FHIR France en 2024 et 2025 - Améliorer la qualité de l’existant</a></li>
            </ul>
        </li>
        <li><a href="#listing-des-acteurs-influen%C3%A7ant-la-trajectoire">Listing des acteurs influençant la trajectoire</a>
            <ul>
                <li><a href="#les-acteurs-dits-politiques">Les acteurs dits &quot;politiques&quot;</a></li>
                <li><a href="#les-acteurs-dits-techniques">Les acteurs dits &quot;techniques&quot;</a></li>
                <li><a href="#les-acteurs-dits-impl%C3%A9menteurs">Les acteurs dits &quot;implémenteurs&quot;</a></li>
            </ul>
        </li>
        <li><a href="#focus-fhir-document">Focus FHIR Document</a>
            <ul>
                <li><a href="#etude-internationale">Etude internationale</a></li>
                <li><a href="#int%C3%A9r%C3%AAt-dusage-du-fhir-document">Intérêt d&#39;usage du FHIR document</a></li>
                <li><a href="#position-de-lagence-du-numerique-en-sant%C3%A9">Position de l&#39;Agence du Numerique en Santé</a><ul>
                <li><a href="#mettre-en-place-une-transformation-entre-les-standards-cda-et-fhir">Mettre en place une transformation entre les standards CDA et FHIR</a></li>
                <li><a href="#permettre-une-utilisation-concomitante-de-fhir-et-de-cda-le-temps-dune-transition-vers-fhir">Permettre une utilisation concomitante de FHIR et de CDA le temps d&#39;une transition vers FHIR</a></li>
            </ul>
        </li>
        </ul>
        </li>
        <li><a href="#actions-men%C3%A9es-pour-encourager-linterop%C3%A9rabilit%C3%A9">Actions menées pour encourager l&#39;interopérabilité</a></li>
        <li><a href="#le-paradigme-document-du-dmp-%C3%A0-compl%C3%A9ter-par-un-service-orient%C3%A9-donn%C3%A9e">Le paradigme &quot;Document&quot; du DMP à compléter par un service orienté donnée</a></li>
    </ul>
</div>

## Introduction à l'interopérabilité

L'interopérabilité est la capacité des systèmes à communiquer entre eux au sein d'un système d'information, qu'il soit local (établissement, GHT), régional ou national, permettant un partage et un accès facilité à une donnée, intégrable, réutilisable et exploitable. L'intérêt stratégique de permettre cette communication pour la e-santé est indéniable, tant pour le patient que pour la recherche clinique.
L'interopérabilité est souvent confondue avec référencement, mais ces termes ne sont pas synonymes. Bien que l'interopérabilité puisse être une exigence dans le cadre d'un référencement, elle se distingue principalement par sa capacité à faciliter le partage et la réutilisation des données. 

Pour faciliter l'accès et le partage de la donnée de santé, il est nécessaire de construire un langage de données informatique uniforme en s'appuyant sur des standards internationaux. La construction d'un langage interopérable valide, utilisable, et qui réponde efficacement au besoin identifié nécessite sa co-construction avec l'ensemble des acteurs de l'écosystème (métier, technique, décisionnaire, politique). Cette collaboration est nécessaire pour valoriser et prioriser une spécification afin d'atteindre le stade ultime de la plus-value pour le médecin et le patient. La clé de la réussite de l'interopérabilité est de fédérer un maximum d'acteurs.
Par la suite, lors du développement d'un logiciel, l'interopérabilité doit être pensée au plus tôt, au moment de sa conception afin d'être "interoperable by design", car une fois des interfaces graphiques développées et corrélées aux flux propriétaires, il est bien plus coûteux de faire l'évolution dans l'autre sens.

## Contexte national

Le déploiement de la e-Santé en France s'appuie sur trois piliers : interopérabilité, sécurité et éthique. L'interopérabilité des systèmes déployés en France est pris en charge par l'Agence du Numérique en Santé (ANS) et d'autres organisations comme l'association Interop'Santé qui est le représentant français des deux principaux organismes internationaux de standardisation HL7 et IHE. L'ANS et Interop'Santé publient les documents de référence définissant les standards à utiliser en France, respectivement le Cadre d'Interopérabilité des Systèmes d'Information en Santé (CI-SIS) et le Guide d'Interopérabilité Hospitalier. Ces deux documents sont parfaitement alignés et cohérents et s'appuient sur des profils d'interopérabilité internationaux d'IHE et de HL7.

Les standards HL7 v2 et CDA ont été créés il y a plusieurs dizaines d'années et sont très robustes mais sont concurrencés par le plus récent standard d'HL7 : FHIR. Il propose une nouvelle façon d'échanger des données par APIs et un protocole d'échange moderne (REST) beaucoup plus proches des technologies modernes de développement informatique. Plusieurs états membres de la communauté européenne font la promotion de standard et les actes d'exécution du règlement européen EHDS seront basés sur FHIR.

L'objectif de ce document est de donner à l'écosystème une vision sur l'évolution des standards d'interopérabilité déployés en France, notamment ceux utilisés par le CI-SIS, dans les programmes nationaux comme le Ségur du Numérique en Santé et les établissements. Cette trajectoire est vouée à évoluer car les travaux sont constants au niveau international et européen. On peut citer par exemple les actes d'exécution du règlement EHDS qui se baseront à priori sur le standard FHIR R4 dans un premier temps mais dont le choix pourrait évoluer.

Pour le moment, ce document traite des standards d'interopérabilité suivants : FHIR, CDA, HL7 V2.

## Stratégie - choix de la version FHIR

La stratégie sur le choix des versions FHIR a été définie au sein d'un groupe de travail organisé entre Interop'Santé et l'ANS en 2023/2024, validée via une [concertation](https://participez.esante.gouv.fr/project/fhir-r5-ou-r4/presentation/presentation) de l'ANS. Les conclusions de ce GT sont indiquées ci-dessous.

### Nouveaux cas d’usages FHIR adressés par Interop’Santé et l’ANS : privilégier FHIR R4 et anticiper la transition vers R6

Pour garantir un écosystème cohérent, éviter tous problèmes de compatibilité ainsi que les travaux divergents, il est nécessaire d'utiliser une même version du standard FHIR à l'échelle nationale. Le choix a été fait de conserver FHIR R4 car il y a un existant conséquent en France et cela permet d'éviter une double transition R4 vers R5 et R5 vers R6. Ce choix est conforté car la release 6 se veut être la “final stable version” de FHIR, une transition vers R6 se voudra de toute manière nécessaire. Pour anticiper cette transition, il est jugé important d’être proactif sur les travaux internationaux de développement de R6 et d’anticiper les impacts pour l’écosystème français.
Il est également à noter que le choix national de la version FHIR utilisée devra être en accord avec le règlement de l'espace européen sur les données de santé (EHDS) qui se dessine progressivement et qui pour l'heure semble se diriger vers R4.

### Ne pas créer de guide d'implémentation (IG) se basant sur R5 sans analyse des normes et standards et des impacts

La priorité actuelle est de faire monter l’écosystème en compétences et de gagner en maturité sur les spécifications existantes. Créer des IGs R5 engendreraient une fragmentation de l’écosystème et un ralentissement de la mise en qualité de l’existant qui finirait par freiner l’adoption de FHIR.

Généralement, rajouter quelques [extensions qui miment les attributs R5](https://hl7.org/fhir/R5/versions.html#extensions) s'avère suffisant pour éviter de créer tout un guide en R5. Dans certains cas, une autre version de FHIR peut être justifiée, par exemple si le cas d'usage concerne des échanges internationaux ou si le cas d'usage est significativement mieux couvert par une autre version. Le cas échéant, l’usage d’une autre version devra être validé par une étude des normes et standards publiée et validée par l’écosystème.

Dans certains cas non identifiés à ce jour, il pourrait également être nécessaire de maintenir des guides d’implémentation sous plusieurs versions. Après validation par l’écosystème de ce besoin, cela donnerait l’opportunité d'estimer des travaux de maintenance d’Implementation Guide (IG) sous plusieurs versions ainsi qu’un mapping associé pour gagner en expérience.

### Priorité FHIR France en 2024 et 2025 - améliorer la qualité de l’existant

De nombreux travaux ont été menés en 2023 pour mettre en qualité les spécifications FHIR et encourager leur déploiement, tel que le passage au format IG et la mise à jour des tests et validateurs gazelle.

Les priorités des prochaines années sont de continuer dans cette direction :

<div class="wysiwyg">
    <ul>
        <li>La montée en compétences et l’acculturation des développeurs et des chefs de projets aux bonnes pratiques d’usages de FHIR, notamment en organisant des évènements par l'ANS et InteropSanté : projectathon, webinaires, formations, ...</li>
        <li>S’assurer de la faisabilité d’implémentation des IGs existants (amélioration du contenu narratif pour expliquer comment utiliser les ressources, s’assurer de la facilité d’accès au contenu, s'assurer que les IGs soient bien connus …).</li>
        <li>Prise en main des outils de mapping tel que le FHIR Mapping Language afin d'assurer une transition maîtrisée vers une autre version de FHIR.</li>
        <li>Anticiper les prochaines évolutions internationales : passage au FHIR Document dans le cadre du règlement européen, anticiper la transition vers FHIR R6, ...</li>
    </ul>
</div>

Il est également nécessaire de rester à l’écoute des tendances internationales en interopérabilité et de se garder la possibilité de réitérer l’analyse si le besoin ou le contexte international évolue, en particulier l'EHDS.

<!-- ## Cartographie de l'interopérabilité -->

## Listing des acteurs influençant la trajectoire

Il est important de prendre en compte qu'il existe de nombreux acteurs qui influencent la trajectoire et que le rôle des experts interopérabilité est d'avoir cette vision globale pour répondre aux besoins en réutilisant au maximum les travaux existants au niveau international, et éviter la nécessité de se ré-aligner par la suite.

Les acteurs peuvent se classifier à plusieurs niveaux : au niveau politique, au niveau modélisation technique et au niveau implémentation.

### Les acteurs dits "politiques"

Ministère de la santé, commission européenne, EHDS

### Les acteurs dits "modélisation technique"

IHE, HL7 International, HL7 Europe

### Les acteurs dits "implémenteurs"

La CNAM (DMP, Mon Espace Santé), les éditeurs de logiciels de soin

## Focus FHIR Document

Aujourd'hui en France, l'ensemble des documents médicaux sont stockés en CDA, notamment avec la plus grande plateforme technique médicale nationale : le DMP, brique de Mon Espace Santé. De son côté, le nouveau standard d'interopérabilité FHIR, particulièrement valorisé pour son API REST, est utilisé dans de nombreux cas d'usages en France : l'annuaire santé, le ROR, le SAS, Mon Espace Santé, ...
Le standard FHIR peut, au même titre que le CDA, être utilisé pour décrire des documents médicaux. C'est par ailleurs la trajectoire qui semble être prise à l'international, notamment par EHDS.

### Etude internationale

Selon l'étude [2024 State of FHIR](../../assets/docs/2024 StateofFHIRSurveyResults_final.pdf), l'utilisation du standard FHIR augmente dans la majorité des pays.

![](../../assets/images/fhir-adoption-rate-change.png)

Cette même étude dévoile un nombre important de pays utilisant le FHIR document.

![](../../assets/images/fhir-documents.png)

De plus, les projets européens European Health Data Space (EHDS) ayant fait une étude de normes et standards pour les échanges transfrontaliers au sein de l'Europe a conclu sur l'usage du FHIR Document. Ce choix est justifié par le fait que certains pays n'ont pas d'historique CDA et choisissent très logiquement d'utiliser le standard FHIR étant plus récent et utilisant des technologies web modernes.
FHIR a été largement préféré par l'Europe pour les trois cas d'usages privilégiés pour le partage transfrontalier : le lab report, l'hospital discharge report et enfin le medical imaging report (resp. 18, 17 et 16 membres préféraient FHIR contre 3, 5 et 5 pour CDA).

### Intérêt d'usage du FHIR document

En plus de la trajectoire internationale semblant mener vers l'usage du FHIR document, des avantages non négligeables sont à noter sur l'usage de ce nouveau standard.

<div class="wysiwyg">
    <ul>
        <li>Les FHIR Document sont composés d'une multitude de brique, appelée ressource (ex : Observation, Patient, Encounter, ...) qui peuvent être extraites du document facilement pour être consommées et réutilisées au sein d'une API Rest par exemple.</li>
        <li>Les spécifications peuvent être publiées en open source sur GitHub car leur édition est totalement en mode texte (FSH / markdown), permettant ainsi de faciliter la collaboration, la remontée d'erreurs, la participation de l'écosystème, l'automatisation des comparaison entre les versions, l'historisation automatique des anciennes versions, ...</li>
        <li>Les spécifications peuvent facilement être héritées d'un contexte international (par exemple le compte-rendu de laboratoire européen peut facilement être adapté pour la France).</li>
    </ul>
</div>

Aux Etats-Unis, les spécifications CDA ont fait leur premier pas vers FHIR, celles-ci sont publiées sont forme de guide d'implémentation en modèle logique, permettant ainsi de valider les CDA avec le FHIR Validator en abandonnant les schematrons [source](https://build.fhir.org/ig/HL7/CDA-ccda/validation.html#:~:text=Validation%20Note-,What%20happened%20to%20the%20Schematron%3F,of%20the%20C%2DCDA%20document.)

L'uniformisation des spécifications d'interopérabilité au niveau européen et modial est un vrai atout pour les entreprises, car cela permet de faciliter leur internationalisation.

### Position de l'Agence du Numérique en Santé

Prioriser la prise en charge du FHIR document est à ce point indéniable, de nombreux indices sur les études internationales et la multiplication de projets lancés mettent en lumière le consensus international sur l'utilisation du FHIR Document.

Deux scénarios de déploiement de FHIR document ont été identifiés en France

#### 1/ Mettre en place une transformation entre les standards CDA et FHIR

Le premier scénario consiste à mettre un place un outil de transformation du standard CDA vers FHIR et inversement.
Cependant, ce scénario nécessité de maintenir cet alignement dans le temps. Les techniques d'alignement sont complexes et lourdes à mettre un oeuvre avec un accroissement de la complexité pour chaque nouvelle version de spécification publiée. Par exemple, des [travaux italiens sur ce sujet](https://www.hl7.it/fhir/cda2fhir/) contiennent plusieurs dizaines de milliers de lignes. Il y a également des questionnements quant à la responsabilité : qui sera responsable du document en cas d'erreur de transformation ?

Pour transformer les documents CDA des volets du CI-SIS vers FHIR, il faudrait que l'ensemble des spécifications CDA soient définies au format StructureDefinition pour utiliser le FHIR Mapping Language.

#### 2/ Permettre une utilisation concomitante de FHIR et de CDA le temps de la transition

Cette solution permettrait une utilisation concomitante de FHIR et de CDA, où les spécifications seront publiées selon les deux modes. Cela permettrait une transition douce avec un timing au choix de chacun vers le passage au paradigme FHIR Document, avec une date limite de décommissionnement de l'autorisation d'écriture en CDA dans le DMP.

Ainsi, au même titre que les documents CDA ne sont pas automatiquement transformés vers les nouvelles versions des spécifications, les documents historiques resteront au format CDA et les nouveaux au format FHIR Document.

La difficulté reviendrait aux consommateurs qui devront, au moins pendant un temps, être capables de traiter deux formats différents : CDA et FHIR. Ce qui ne changerait pas de la situation actuelle finalement car les spécifications CDA évoluent elles aussi.

#### Solution privilégiée par l'ANS

La solution qui semble se dessiner pour l'ANS est de permettre une utilisation concomitante de FHIR et de CDA pour faire une transition douce, complétée d'une preuve de concept d'un mapping CDA - FHIR, générique, sans aller jusqu'à une spécification validée et utilisable en production, pour aider les éditeurs dans leur transition.

## Actions menées pour encourager l'interopérabilité

De nombreuses actions sont menées pour faciliter l'usage des standards et l'interopérabilité en France.

### La plateforme de tests gazelle

La plateforme de tests gazelle permet à chaque concepteur de logiciels de tester sa conformité aux spécifications d'interopérabilité du CI-SIS. Celle-ci est ouverte en permanence à l'adresse [https://interop.esante.gouv.fr/evs/home.seam].

### Le serveur multi terminologique (SMT)

Le serveur multi terminologique est un site web permettant d'accéder à l'ensemble des terminologies et jeu de valeurs à utiliser en France. Il dispose également d'une API pour accéder informatiquement à ces informations. Le SMT est accessible à l'adresse [https://smt.esante.gouv.fr/]

### GitHub

L'ANS prône la démarche open source et publie la majorité de ses spécifications sur GitHub. GitHub permet à n'importe qui d'accéder à notre code source et à écrire des commentaires dans une perspective d'amélioration continue.
L'organisation ANS sur GitHub est accessible à l'adresse[https://github.com/orgs/ansforge/dashboard].

### Les projectathons

L'ANS organise régulièrement des projectathons, évènement unique permettant à tous les éditeurs de se rencontrer et de tester ses interfaces d'interopérabilité en point-à-point.
Notre plateforme de tests gazelle est utilisée dans le cadre de ces évènements.

## Le paradigme "Document" du DMP à compléter par un paradigme "API

L'historique français avec le DMP montre le cas d'usage "document" : un document est un compte rendu médical signé et daté d'un patient. Il est possible de voir un nouveau cas d'usage qui n'est pas orienté document mais plutôt un paradigme "API".

Il y a par exemple déjà actuellement les API Mesures de santé et Agenda de Mon Espace Santé où il y a des données accessibles via des requêtes REST sans document médical.

Ainsi, il ne faudra pas négliger ce paradigme API REST pour certains cas d'usages s'y prêtant bien, comme par exemple une API de vaccination, une API Cercle de Soins, une API pour la diffusion des essais cliniques ouverts au recrutement. L'intérêt tout particulier de ce type d'API réside sur l'utilisation de critères de recherches standards définis par FHIR pour accéder à l'information d'intérêt simplement, sans superflu.
