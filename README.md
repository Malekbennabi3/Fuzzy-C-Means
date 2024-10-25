# Fuzzy-C-Means
Implementation de l'algorithme Fuzzy C-Means pour un [TP du module Reconnaissance des formes](https://github.com/Malekbennabi3/Fuzzy-C-Means/blob/main/Enonc%C3%A9%20TP.pdf) (M2 VMI- FI)

## Algorithme
Le Fuzzy C-means (FCM) est une méthode de Clustering (regroupement) qui permet à une donnée d'appartenir à deux groupes ou plus. 
Cette méthode (développée par [Dunn en 1973](https://doi.org/10.1080/01969727308546046) et améliorée par [Bezdek en 1981](https://doi.org/10.1007/978-1-4757-0450-1)) est fréquemment utilisée dans la reconnaissance des formes. Elle est basée sur la minimisation de la fonction objective suivante :

$$ F_m=\sum_{i=1}^{N}\sum_{j=1}^{C}u_{ij}^{m}\left\| x_i-c_j \right\|^{2}  \quad , \quad   1\le m\le \infty $$

où:
- m est un nombre réel supérieur à 1
- uij est le degré d'appartenance de xi à la classe j, 
- xi est la i-ème des données mesurées d-dimensionnelles, 
- cj est le centre d-dimensionnel de la classe.

## Etapes d'Execution

1- Initialiser la matrice $U<=[u_{ij}] \quad , U^{(0)}$

2- À l'étape k : calculer les vecteurs de centres $C^{(k)}=[c_j] \quad avec \quad U^{(k)}$

  $$ C_j=\frac{\sum_{i=1}^{N}u_{ij}^m.x_i}{\sum_{i=1}^{N}u_{ij}^m} $$

3- Mettre à jour $U^{(k)}, \quad U^{(k+1)}$

$$ u_{ij}=\frac{1}{\sum_{k=1}^{C}(\frac{\left\| x_i-c_j \right\|}{\left\| x_i-c_k \right\|})^{\frac{2}{m-1}}} $$

4- Arreter Si $\left\| U^{(k+1)}-U^{(k)} \right\|\le \epsilon$ 
    Sinon retourner à l'etape 2

## Image Originale vs Image après segmentation

<div align="center">
  <img src="https://github.com/Malekbennabi3/Fuzzy-C-Means/blob/main/milky-way-nvg.jpg" width="400" height="400">
  <img src="https://github.com/Malekbennabi3/Fuzzy-C-Means/blob/main/Images%20segmentees/segmentation_iter_11.png" width="500" height=500">
</div>
