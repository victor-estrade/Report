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

![Moon classique](fig/moon-bound-0.png)

|Info/couche   |Dense (1)  |Dense (2)  |
|:------------ |:----------|:----------|
|nb neurone    |3          |2          |
|Activation    |tanh       |softmax    |
|Learning rate |1.0                    |
|Initialisation|Glorot (défaut)        |



On peut simuler un problème d'adaptation en applicant une petite transformation
sur ces données.

Rotation
--------

Avec une rotation de 35 degrés le réseau de base perd une partie de ses performances.

![Moon après une rotation de 35 degrés. Les performances ont diminuées.](fig/moon-rot-bound-0.png)

En applicant un DANN on peut partiellement corriger ce problème ($\lambda_D=0.7$)

![Moon après une rotation de 35 degrés. En utilisant un DANN.](fig/moon-rot-bound-1.png)

![Moon (donnée originale). Le DANN ne fait pas perdre de performances sur ce datasaet.](fig/moon-bound-1.png)


Matrice à dominance diagonale
-----------------------------

Une autre transformation consiste à appliquer une matrice à dominance diagonale
aux données:

$$ x \gets A.x $$
où $A$ est une matrice $(2\times2)$ générée aléatoirement.

![Moon après transformation. Sans utilisation du DANN](fig/moon-A-bound-0.png)

![Moon après transformation. En utilisant le DANN](fig/moon-A-bound-1.png)
