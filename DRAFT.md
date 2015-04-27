# Patate vs. Pommes de terre : ça va se friter !

## Introduction

Anecdote de Thomas sur son restaurant moisie de patates qui a finalement été un
restaurant 5 étoiles ("écrasé de pommes de terre")

### Définitions

* Définir "efficacité" : la manière de faire une tâche en dépensant le moins de ressources possible
* Définir "beauté" : la manière de faire une tâche en répondant au plus de critères de qualité possible

### On se posait une question

 > Est-ce que j'allie correctement la beauté et l'efficacité ?

## Mise en situation

Projet du client : faire une application d'adoption de chatons

### 1. POC
_+++ efficacité_

On cherche à satisfaire le budget et la deadline du client

Triangle de merde : cheap / good / fast

c'est positif

_exemple de ce qui peut être fait full efficacité_

### 2. Passons le POC en prod !
_++ qualité_

- il plante (stabilité)
- rajouter des features est très couteux (évolutivité)
- risqué/compliqué de mettre en prod

On se rend compte à quel point c'est problématique

- je suis vexé et déçu, je refais tout from scratch en ultra qualité (je vais
pas retomber dans le piège comme même)

_exemple de ce qui peut être fait en full qualité_

On peut tout faire sur le papier ! Mais on l'a pas fait ...

#### Done is better than perfect

\*Nothing like a BBC

### 3. Merde, la release, c'est dans 2 mois ...
_+efficacité_

On drop les tests
On double l'équipe

On commence à prendre des raccourcis de code (exemple : ah bah non, pas de
commande pour ça), ajouter des exceptions

_exemple : on arrête de faire des commandes handlées par les bus_

### 4. Il faut maintenir le projet
_efficacité = qualité_

On tend à améliorer la qualité pour combler les lacunes dues au rush

Prendre des petits scopes et les améliorer au fur et à mesure, à l'occasion d'un
besoin de modification. On amortit le coût de la qualité petit à petit, par la
petite valeur que ça produit

_exemple : event sourcing maison sur les grosses requêtes SQL. On contacte un
module qui a précalculé les valeurs et qui peut les renvoyer avec de bonnes
perfs. Et ce, agrégé par ton controller_

## Et le prochain projet ?

On recommence, en essayant à chaque fois d'adoucir les extrèmes.

## Est-ce que j'allie correctement la beauté et l'efficacité ?

Suivant l'exigence du projet en terme de performance, de durée de vie, les
impératifs de qualité du client

Est-ce que ce niveau de qualité est nécessaire pour la feature ?
Est-ce que ce niveau de qualité va engendrer une trop grande dette technique ?

Monitoring du résultat via les valeurs du HUD

_scene où le débile dit qu'il est juste dev, et que c'est bien mignon, mais que
c'est pas son boulot_

## C'est le métier de dev

Finalement, est-ce que ce ne serait pas notre métier de dev ?
De lever le nez de son code, faire attention au contexte, aux gens qui nous
entourent. Et bouger pour que tout ça soit dans le vert ?

\#CareAboutYourStuff

## Crédits

Je suis Thomas Jarrand @tom32i
Je suis Emeric Kasbarian @emerick42

Et on développe des projets chez élao





HUD sur les caractéristiques du projet :
* Motivation de l'équipe
* Valeur du produit
* Dérivée de l'avancement par rapport au moment T
* Dette technique
* Taux de crâmage du budget
* Contentement du client
