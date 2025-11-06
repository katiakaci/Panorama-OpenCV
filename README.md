# Panorama avec OpenCV 📸

Ce projet présente une application Python utilisant OpenCV pour fusionner plusieurs images prises sous différents angles afin de créer un panorama complet, à la manière des téléphones intelligents. Il inclut également une étape de recadrage automatique pour supprimer les bordures noires et obtenir une image finale propre.

Pour créer l'application de base, le tutoriel suivant a été suivi : [Image Stitching with OpenCV and Python](https://pyimagesearch.com/2018/12/17/image-stitching-with-opencv-and-python/)

## Aperçu du projet

Ci-dessous un exemple : images d'entrée tirées de `images/Test1/` et le panorama de sortie dans `resultats/Test1/`

| Images d'entrée | Résultat |
|---|---|
| ![entrée 1](images/Test1/PXL_20250202_234440928.jpg)<br>![entrée 2](images/Test1/PXL_20250202_234443703.jpg)<br>![entrée 3](images/Test1/PXL_20250202_234446223.jpg) | ![résultat](resultats/Test1/output_final.png) |


## Lancer le script

1. Placer les images dans un dossier du type `images/TestX/`
2. Lancer le stitching avec :

```powershell
python image_stitching.py --images images/TestX --output resultats/TestX/output_final.png --crop 1
```

- `--images` : chemin du dossier contenant les images source
- `--output` : chemin du fichier de sortie
- `--crop` : 1 pour activer le recadrage automatique, 0 pour le désactiver

## Fonctionnalités principales

- Fusion automatique d’un ensemble d’images en un panorama
- Alignement des images basé sur l’algorithme SIFT
- Détection et correction des contours noirs internes
- Recadrage automatique du panorama final

## Références

- Brown, M., & Lowe, D. G. (2007). Automatic Panoramic Image Stitching using Invariant Features.
- Rosebrock, A. (2018). Image Stitching with OpenCV and Python. PyImageSearch Blog.
- Kennerley, M. (2021). Comparing SIFT and ORB for Feature Detection.