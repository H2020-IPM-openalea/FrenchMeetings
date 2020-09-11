---
ms.date: 09/03/2020
---

# IPM-Décision meeting report

## Reunion du 09/09/2020: WP2 format metadata Json-LD

### Présent

Tor-Einar, Christophe Pradal, Marc Labadie

### Objectif
Discution sur le formats JSON-LD, reponse au interrogation de Tor-Einar

### Discussion

Le format JSON-LD a des avantages mais ne seras peut etre pas utilise dans le contexte IPM car
VIPS est un object base sur Json schema il faudrait pouvoir transformer tous les schema de VIPS en JSON-LD?

Tor vois bien l'utilite du JSON-ld mais il faut faire des preuves.

### Tache
Des Tasks nous ont ete assigne durant la reunion via [JIRA](https://nibio.atlassian.net/)

* [Task 1](https://nibio.atlassian.net/jira/software/c/projects/IDEC/issues/IDEC-117?filter=allissues): Create Json schema with Json-ld integrated for DSS and DSS_model

* [Task 2](https://nibio.atlassian.net/jira/software/c/projects/IDEC/issues/IDEC-118?filter=allissues) : Create IPM DSS compatible web service for OpenAlea

### Demande/ Questions / Remarque

* Tor aimerai que l'on mette rapidement un model openalea sur VIPS
* Les models et les donnees meteo sont disponible et utilisable

## Reunion du 03/09/2020: WP3 Reunion Planning IPM

### Présent

Christian Fournier, Christophe Pradal, Marc Labadie

### Objectif
Definir le plan d'action pour le projet IPM et organisation du travail

### Tâches

1. Définir un use case

    1.1 Modèle simple package/node pur Python

    * permet de tester toute la chaine simplement (import / export openalea/IPM)
    * Export au format JSON-LD
    * creation dynamique de web service
    * déploiment docker/IPM

   1.2 Use case complex

    * septo/wheat
    * modèle composite qui permet de tester l'assemblage
    * plante simplifiée (LAI? voir avec Corinne)
    * définition du schéma intégration
    * extension à une version simplifiée d'ECHAP?
    * Schema d'integration de Guillaume (ALEP) et de Corinne

2. Import / Export IPM

    2.1 Export vers IPM
    * schéma JSON-LD
    * execution web service
    * ...

    2.2 Import d'IPM
    * execution d'un web service en tant que neoud OpenAlea
    * gestion données (météo)

    2.3 Implementatio d'un tuto
    * PS: Voir les déliverables...

>**NOTE TO INSTALL VISUALEA**: 
> * Pour Visualea: Dans la console ou le .bashrc taper export QT_API_VERSION=2
> * environement description: 
>   * qt4, Pyqt, (qtconsole 4.3)
> * conda install: 
>   * numpy (1.14 max pour rpy2 sous linux), pandas, alinea.caribu, openalea.plantgl,scipy, rpy2,alinea.astk, pvlib-python, openalea.sconsx
> * pip install: matplotlib (conflit avec conda)
> * python setup.py develop (en mode develop): 
>    * echap ,weather,septo3d,popdrops  (gforge INRIA) 
> * python setup.py install a partir de git: 
>   * openalea.mtg, astk (plutot cavec conda), adel 

### Organisation du travail
* Une fois par semaine (le jeudi) Marc ou christian se retrouve soit a INRAE soit au CIRAD pour travailler ensemble sur le projet 
* Une fois par mois seance de coding spring

## Reunion du 17/06/2020: WP2- Réunion sur le amélioration du schéma (JSON-LD)

### Présent

Tor-Einar, Christophe Pradal, Marc LABADIE

### Objectif

* Amélioration communication entre model utilisation de JSON-LD pour définir un schema. 

### Discussion

* Proposition d'un schema en JSON-LD à Tor-Einar afin d'avoir un standard entre les modèles. Sur la base de [codemeta](https://codemeta.github.io/) et schema.org 
* Cette proposition participera au WP3 et permettra une communication entre les modèles simplifié.

### Tâches

* [X] Proposer un schema JSON-LD  permettant de liér les différents modèle. (pour le 16 juillet 2020)
  
## Reunion du 11/06/2020: Discussion sur le projet IPM

### Présent

Christian Fournier, Christophe Pradal, Marc LABADIE

### Objectifs

Discussion sur le projet

### Discussion

* deliverable:

  * faire un schema integration autre maladie à partir de open alea
  * modèle aide à la decision, données climatique - maladie - pheno si possible.

* Papier
2 papiers model:
  * papier IPM (format, donnée standardiser), à lier avec OpenAlea
  * ECHAP 2013:
    * publi logiciel
    * publi en cours

Christophe reserver pour le papier.

* modèle à prévoir
* simple wheat
* modèle maladie

### Tâches

Prendre ALEP modifier simplifier interface (ALEP sera appelé EPI3D)

* faire un simple wheat (contrôle tallage, scenescence)
* interface maladie

Christian et Christophe

* [ ] mise à jour ALEP passage en python 3 et sur Github
* [ ]  modèle simple céréales
* [ ] liste des modèle disponible

Marc:

* [ ] en attente de passage des modèles en python 3 et de la liste des modèles
* [ ] regarder les modèles présent dans ALEP
* [ ] Réflexion sur un interface simple des modèles
* [ ] biblio

## Reunion du 05/06/2020: IPM-Decision postdoc meeting

### Présenton

Corinne Robert, christian Fournier, Christophe Pradal, Marc Labadie

### Objectif

* Discussion sur le projet IPM-Decision (post doc Marc) -- point d'information & suite

### Discussions

* Délivrable: (en attente d'envoie par christian)

* repartition du temps de marc approximatif
  * 6 mois mi temps avec Christophe sur WP2
  * 6 mois finalisation des modèles ECHAP, septo3D.

ECHAP: simplifier les modèles documentation
reprendre ALEP3D/SEPTO3D/RUST3D+RUSTSEPTO3D+VIGNE=EPI3D, simplifier réimplémenter

objectif: le modèle simplifier cropmodel comparaison avec un autre modèle simplifier.

Question Corinne: Garder architecture garder la senescence.

Part: quel est l'impact de le l'architecture sur l'épidémie

_3 modèles:_

* simplifier
* cohorte
* FSPM

_IPM:_
Travail sur 1 selection de DSS

Distribution de classe d'age pour la maladie, pas de retroaction de la maladie

### Publications

* publi ECHAP 2013, publi interception analyse de sensibilité. Tout echap très gros.
* publi logiciel ECHAP (tous les modèles soit publié, comment faire dialogué les modèles)
* publi ADAS

### Tâches définies

* [ ] simplifier modèle (Utilisation, calcul, hypothèse), faire un bilan Regarder tous les paramètres, Quelles sont les leviers a actionner, (pb paramétrage infini)

### Questions

Comment rendre le modèle plus simple en utilisation?
Quels sont les paramètres nécessaire aux utilisateur? (evolution de la surface au cours du temps)

1. Quel est l'impact de l'architecture sur la maladie? (modèle maniable? mélange maladie, sensibilité de la surface foliare. mettre les blé en mélange? )
2. Modèle arriverait en compétition des isolats d'une maladie, histoire selection adaptation.

Modèle possible modèle classe d'age en couche de corinne avec paramètres de modulation des paramètres maladie avec ou sans retro-action (retro-action sur la vitesse de développement (surface verte))
Modèle architecturale classe d'age, vitesse de développement, champignon, variétale

Corinne quel entrée quel sortie?
Dynamic de la mise en place de couvert impact la maladie avec des variables d'entré, de sortie pour une utilisation simplifier

### Résumer christophe pradal

Voici mon résumé:

1. Travailler sur les déliverables:

* représenter les modèles/données/assemblage en json-ld
* bibliothèque Python pour transformer/appeler/executer les services de la plateforme IPM

2. Modèle Epi3D (<https://github.com/openalea-incubator/alep>)

a. Ressuciter le modèle (install, documentation, tutorial)

b. définir une interface simple pour piloter le modèle (septo)

* comparer le même modèle en SEIR ou architecturé

c. possibilité de simplifier l'architecture:

* paramètres: simple wheat (archi mais avec paramètres simplifié)
* representation: prendre en compte l'archi mais de façon implicite (surface foliaire / classe age)
* full: mixture

Une question me reste:
Est-ce qu'on peut aussi profiter de la période pour finaliser un travail qui serait "presque" fini?

## Reunion du 11/05/2020: IPM-Decision Format

### Présent

Tor-Einar Skog, Christophe Pradal, Marc Labadie

### Objectifs

Liens vers le documents: <https://github.com/H2020-IPM-openalea/formats/blob/master/DSS_metadata/fields.md>

* Discussion sur les formats (champs) des trois modèles DSS, OpenAlea, Crop2ML. Etude comparative des champs des trois modèles.
* Identification d'un formalisme pour les trois modèles avec des champs commun.

### Discussions

Ce qui en ressort est une adaptation mixte entre format DSS model et  OpenAlea.

> **NOTE:**  Tor-Einar devrait nous faire un retour avec une proposition de format

## Réunion du 24/04/2020: IPM-Decision, Réunion debut du post doc de Marc

### Présent

Christophe Pradal, Christian Fournier, Corrine Robert, Marc Labadie

### Objectifs

* Réunion de rentrée discussion sur le projet et les choses à mettre en place
* RDV à venir : Annual IPM meeting 27-29 avril.

### Discussions

* Descriptif du poste :

  * Post doc très informatique, simplifier les modèles, réfléchir une structure informatique, utilisation de variable d’entrer, variable globale
  * Mise en place des modèles en plateformes. Mise en disposition des modèles. Comparaison avec différente spécificités

* Tâches :

  * Normaliser les données météo. WP2 interphase standardisation plateforme.
  * Formalisme des modèles, catalogue du modèle (très techniques), donnée, métadonnées météo en place. Catalogue Affichage des modèles
  * Définir des standards interaction avec eux. (Faire des container, développement logiciel)
  * A partir du modèle IPM interface unifié organisation modèle plante maladie. 4 -5 modèle IPM de montrer que tu peux faire un modèle simplifier.

* Publications envisager :

    1. Papier bio ECHAP à finir Reprendre l’existant l’ECHAP (2010-2012). Archi et épidémie colorant sur 3 ans modèle d’interception
    2. papier septo3D multi-échelle modèle de plantes 3D
    3. papier echap logiciel

### Todo (Marc)

* [X] Prise de connaissance des documents existant
  * [X] Lecture bibliographiques
    * [X] Echap 2013
    * [X] Garin et al 2014
    * [X] Powerpoint 2013 et 2016

  * [X] Participation Annual meeting
    * Lundi 13h30-15h00: IPM Decisions - Project update (Chair: Neil Paveley (ADAS))
    * Mardi 10h00-11h30: WP2 & 3 joint session - API Developing and testing Chair: Berit Nordstrog (NIBIO)
    * Mardi 14h00-15h30: WP 2, 3 & 4 joint session - DSS data input and output requirements Chair: Dave Skirvin (ADAS)

### Questions

* Il serait bien de ce prévoir une réunion le 4 mai afin de définir les différentes tâche que je dois réaliser, au moins pour me lancer sur le postdoc
* Avez vous réussi a télécharger les vidéos de présentation ainsi que les présentations? J'aimerai les garder afin de me les repasser si nécessaire pour bien comprendre le projet.
