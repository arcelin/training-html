# 02 - Progress steps

## JS

- **Sélectionner un élément à partir de son id depuis un fichier HTML.**

```js
const progress = document.getElementById("progress");
```

- **L'égalité stricte :** utiliser la plupart du temps `===` au lieu de `==` dans les comparaisons. L'égalité non stricte(`==`) va pouvoir comparer des objets de types différents : par exemple, `0 == false` va retourner `true`, mais `0 === false` va retourner `false`.

```js
if (currentActive === circles.length) {
  next.disabled = true;
}
```

- **Changer une valeur d'un élément de CSS :** les valeurs CSS sont interprétées comme des éléments String.

```js
progress.style.width =
  ((actives.length - 1) / (circles.length - 1)) * 100 + "%";
```

## CSS

- `:root` : représente la première balise `<html>`. Permet la définition de variables globales dans le CSS, réutilisables partout. Plutôt utile pour appliquer certaines chartes graphiques ! Les noms des variables s'écrivent avec deux tirets `-`. Appeler une variable se fait avec le mot-clé `var`.

```css
:root {
  --line-border-fill: #3498db;
  --line-border-empty: #e0e0e0;
}

.btn {
  background-color: var(--line-border-fill);
}
```

- `::before` et `::after` : applique le CSS juste avant ou juste après la balise concernée. Dans cet exercice, le `progress-container` est en deux parties : la partie grise, déterminée par le `::before`, et la partie bleue qui progresse avec le JavaScript.

```css
.progress-container::before {
  content: "";
}
```

- `transform` : utilisé pour appliquer des effets particuliers à des objets HTML.

```css
.progress {
  transform: translateY(-50%);
}
```
