# Steganographie d’images (Pillow)

Ce script cache une image `.png` dans une autre en utilisant les bits de poids faible (4 bits) des canaux RGB, puis permet de la récupérer.

## Prérequis
- Python 3
- Pillow : `pip install pillow`

## Dossiers attendus
Le programme attend **exactement 1** fichier `.png` dans chaque dossier :
image_de_base/image_visible/
image_de_base/image_cache/
image_a_decoder/

## Utilisation
1. Mets une image dans `image_de_base/image_visible/` et une autre dans `image_de_base/image_cache/`.
2. Lance : `python ton_script.py` → génère `code.png`.
3. Mets `code.png` dans `image_a_decoder/`.
4. Relance : `python ton_script.py` → génère `decode.png`.

## Sorties
- `code.png` : image “visible” contenant l’image cachée.
- `decode.png` : image cachée reconstruite (qualité réduite car seulement 4 bits/canal).
