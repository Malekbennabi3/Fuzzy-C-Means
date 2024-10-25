# Fuzzy-C-Means
Implementation de l'algorithme Fuzzy C-Means pour le module Reconnaissance des formes (M2 VMI- FI)

## Algorithme
Le Fuzzy C-means (FCM) est une méthode de Clustering (regroupement) qui permet à une donnée d'appartenir à deux groupes ou plus. 
Cette méthode (développée par Dunn en 1973 et améliorée par Bezdek en 1981) est fréquemment utilisée dans la reconnaissance des formes. Elle est basée sur la minimisation de la fonction objective suivante :

$$ F_m=\sum_{i=1}^{N}\sum_{j=1}^{C}u_{ij}^{m}\left\| x_i-c_j \right\|^{2}  \quad , \quad   1\le m\le \infty $$

où:
- m est un nombre réel supérieur à 1
- uij est le degré d'appartenance de xi à la classe j, 
- xi est la ième des données mesurées d-dimensionnelles, 
- cj est le centre d-dimensionnel de la classe.

## Etapes d'Execution

1- Initialiser la matrice $U<=[u_{ij}] \quad , U^{(0)}$

2- À l'étape k : calculer les vecteurs de centres $ C^{(k)}=[c_j] avec U^{(k)} $

## Image Originale vs Image après segmentation

<div align="center">
  <img src="https://github.com/Malekbennabi3/Fuzzy-C-Means/blob/main/milky-way-nvg.jpg" width="400" height="400">
  <img src="https://github.com/Malekbennabi3/Fuzzy-C-Means/blob/main/Images%20segmentees/segmentation_iter_11.png" width="500" height=500">
</div>
