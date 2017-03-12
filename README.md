# GEC = Garé En Chiasse

_French only (for the moment)._

_WIP / Travail en cours._

## Objectif

L'objectif de ce dépôt est de réunir idées, reflexions et solutions quant à la mise en oeuvre d'un outil de déclaration de véhicules "garés en chiasse", c'est à dire (très) mal garés, tel que : sur un [trottoir](https://fr.m.wikipedia.org/wiki/Trottoir), sur une [piste cyclable](https://fr.m.wikipedia.org/wiki/Am%C3%A9nagement_cyclable#Piste_cyclable), sur un [passage piéton](https://fr.m.wikipedia.org/wiki/Passage_pi%C3%A9ton), etc.

Pour ce faire, l'outil devra être simple d'utilisation et mobile.
Ainsi, une application pour téléphone mobile (iOS et Android) semble le plus adaptée.

De plus, afin de permettre une exploitation des données collectées via de multiples supports, il apparait judicieux que ces données soient stockées et accessibles via un service en ligne (donc via une API normalisée).

## Conception fonctionnelle et UX

### Données

| Intitulé   | Description                      | Requis |
|------------|----------------------------------|--------|
| id         | L'identifiant unique             | Oui    |
| date       | La date et l'heure de la collecte| Oui    |
| photo      | La photo prise par l'utilisateur | Oui    |
| utilisateur| L'identifiant de l'utilisateur   | Oui    |
| longitude  | La longitude                     | Oui    |
| latitude   | La latitude                      | Oui    |
| adresse    | L'adresse postale                | Non    |
| type       | ex: "trottoir", "piste cyclable" | Non    |
| catégorie  | La catégorie du véhicule         | Non    |

Concernant la catégorie du véhicule, se référer à [_La définition des catégories de véhicules_](http://www.developpement-durable.gouv.fr/La-definition-des-categories-de,12402.html).

### Écrans (wireframes)

_À faire._

### Diagramme de flux

_À faire._

## Conception technique

### Application mobile

La technologie envisagée est [React Native](https://facebook.github.io/react-native/), qui combine plusieurs avantages, dont :

1. un même coeur "métier" quelque soit la plateforme visée (approche hybride)
2. une construction par composant natif afin de garantir une expérience utilisateur efficace

### Serveur

Le serveur de l'application (l'[API](https://fr.m.wikipedia.org/wiki/Interface_de_programmation)) s'appuyera sur le protocole [REST](https://fr.m.wikipedia.org/wiki/Representational_state_transfer) pour des raisons évidentes d'interopérabilité.

Il sera ainsi possible d'alimenter et d'exploiter les données via différents frontends : l'application mobile, mais aussi un site 
Web "classique", proposant une vue carte par exemple.

#### Solutions techniques envisagées

##### Auto-hébergé

1. [Apigility](https://apigility.org) (PHP)
2. [API Platform](https://api-platform.com) (PHP)
3. [LoopBack](https://loopback.io) (Node.js)

##### [SaaS](http://fr.wikipedia.org/wiki/SaaS)

1. [Firebase](https://firebase.google.com)

## Annexes

### Législation

Il semblerait (à documenter) qu'il ne soit pas possible de collecter des numéros de plaques d'immatriculation et de les rendre public.

Aussi, une solution envisageable serait de collecter les numéros de plaque mais de les [obfusquer](https://fr.wiktionary.org/wiki/obfusquer) lors de la consultation.
Ainsi, il serait possible d'effectuer des statitiques - anonyme - sur la féréquence d'identification d'un numéro de plaque d'immatriculation, sans pour autant la rendre visibile sur les photos.

### Initiatives comparables

* https://github.com/mathieuruellan/gcummap
* https://github.com/glullien/GCUMFisherAndroid (par [@glullien](https://twitter.com/glullien) et [@veloklash](https://twitter.com/veloklash))
* https://github.com/infinitesunrise/carsinbikelanes (https://carsinbikelanes.nyc)
* https://github.com/jessamynsmith/my-bike-lane-mobile (https://mybikelanemobile.herokuapp.com)

## Licence

MIT License

Copyright (c) Arnaud Ligny
