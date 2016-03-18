---
title: DANN with some toy datasets
author: Victor
header-includes:
    - \usepackage{preambule}
abstract: This is a pandoc test . . . 
---

Moon dataset
============

L'exemple des 2 lunes imbriquées est un problème non linéaire simple.
Un réseaux de neurone à 1 couche caché de 3 neurones permet de le résoudre.

![Moon-bound-0](fig/moon-bound-0.png)



On peut simuler un problème d'adaptation en applicant une petite transformation
sur ces données.

Rotation
--------

Avec une rotation de 35 degré le réseau de base perd une partie de ses performances.

![Moon-rot-bound-0](fig/moon-rot-bound-0.png)

En applicant un DANN

Matrice à dominance diagonale
-----------------------------


### Useless Sub-sub-section
