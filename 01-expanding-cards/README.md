# 01 - Expending cards

## Notes

### HTML

- `background-image` : l'exercice ici est d'afficher l'image non pas dans une balise html `<img>`, mais dans une balise `<div>` en utilisant l'attribut `style`.

```html
<div
  class="panel"
  style="background-image: url('./images/demon-slayer.jpg');"
></div>
```

### CSS

- **Unités relatives en css** : on a l'habitude d'utiliser les classiques `px` ou `mm`, mais dans le corrigé, il utilise les unités `vh` et `vw` qui représentent les pourcentages de l'élément par rapport à la hauteur (height) ou la largeur (weight). Documentation : <https://www.w3schools.com/CSSref/css_units.asp>.

```css
.container {
  width: 90vw;
}
```

- `flex` : les images de background n'ont aucune largeur définie, seul le container en a une. On utilise la classe `active` dans le css pour définir un paramètre `flex` égal à 5.

```css
.panel.active {
  flex: 5;
}
```

- `transition` : dans le css, donne cet effet de transition smooth au moment où le panel actif change.

```css
.panel {
  transition: all 700ms ease-in;
}
```

- `position: relative` : définit le positionnement de l'élément contenu dans l'élément englobant.

```css
.panel {
  position: relative;
}
```

### JavaScript

- Sélectionner les éléments d'un fichier HTML depuis le JavaScript.

```js
const panels = document.querySelectorAll(".panel");
```

- `classList` : permet la manipulation des éléments d'une classe HTML depuis le JavaScript.

```js
panel.classList.add("active");
```

### Autres

- [imgix](https://dashboard.imgix.com) : API d'accès à des images. Les fichiers sont hébergés sur des solutions de stockage Cloud comme Amazon S3, Google Cloud Storage ou autre. En passant certains paramètres dans l'URL, il est possible de modifier l'image au moment où la requête est effectuée. Pour l'exercice, j'ai choisi d'utiliser des images téléchargées et stockées localement dans le dossier `/images`.
