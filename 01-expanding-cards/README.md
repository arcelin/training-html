# 01 - Expending cards

## Améliorations à apporter

- Remplacer les titres des images par les logos des séries au format png.
- Ajouter des fragments de code dans le README avec les bonnes balises.

## Notes

- [imgix](https://dashboard.imgix.com) : API d'accès à des images. Les fichiers sont hébergés sur des solutions de stockage Cloud comme Amazon S3, Google Cloud Storage ou autre. En passant certains paramètres dans l'URL, il est possible de modifier l'image au moment où la requête est effectuée. Pour l'exercice, j'ai choisi d'utiliser des images téléchargées et stockées localement dans le dossier `/images`.
- `background-image` : l'exercice ici est d'afficher l'image non pas dans une balise html `<img>`, mais dans une balise `<div>` en utilisant l'attribut `style`.
- **Unités relatives en css** : on a l'habitude d'utiliser les classiques `px` ou `mm`, mais dans le corrigé, il utilise les unités `vh` et `vw` qui représentent les pourcentages de l'élément par rapport à la hauteur (height) ou la largeur (weight). Documentation : <https://www.w3schools.com/CSSref/css_units.asp>.
- `flex` : les images de background n'ont aucune largeur définie, seul le container en a une. On utilise la classe `active` dans le css pour définir un paramètre `flex` égal à 5.
- `transition` : dans le css, donne cet effet de transition smooth au moment où le panel actif change.
