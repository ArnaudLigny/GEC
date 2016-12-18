# GEC = Garé En Chiasse

_French only (for the moment)_

L'objectif de ce dépôt est de réunir idées et relfexions sur la mise en oeuvre d'un outil de déclaration de véhicules "garés en chiasse",
c'est à dire (très) mal garés : sur un trottoire, sur une piste cycable, sur un passage piéton, etc.

Pour ce faire, l'outil devra être simple et mobile. Ainsi, une application pour téléphone mobile (iOS et Android) semble le plus adaptée.

De plus, afin de permettre une exploitation des données collectées via de multiples support, il semble judicieux que ces données 
le soit via un service en ligne, donc via une API normalisées.

## Approche technique

### Application mobile

La technologie envisagée est [React Native](https://facebook.github.io/react-native/), qui combine plusieurs avantages, dont :

1. un même coeur "métier" quelque soit la plateforme visée (hybride)
2. une approche par composant natif afin de garantir une expérience utilisateur efficace

### Backend

Le backend de l'application, l'API, s'appuyera sur le protocole [REST](https://fr.m.wikipedia.org/wiki/Representational_state_transfer).

Solution techniques envisagées :

1. [Apigility](https://apigility.org)
2. [API Platform](https://api-platform.com)

Il sera ainsi possible d'alimenter et d'exploiter les données via différents frontend, l'application mobile, mais aussi un site 
Web "classique", proposant une vue carte.

## Points d'attention

### Législation

Il semblerait (à détailler) qu'il ne soit pas possible de collecter les plaques d'immatriculation et de les rendre public.
Aussi, une solution envisageable serait de collecter les numéros de plaque mais de les [obfusquer](https://fr.wiktionary.org/wiki/obfusquer) 
lors de la consultation.
Ainsi, il serait possible d'effectuer des statitiques sur la féréquence d'idnetification d'une plaque d'immatriculation, sans pour 
autant la rendre visibile sur les photos.

_WIP_

## Licence

MIT License

Copyright (c) 2016 Arnaud Ligny
