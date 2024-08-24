# SASS

## Syntactically Awesome Style Sheets

### CSS with superpowers

Sass é um préprocessador de css que possuí ferramentas que não existem no mesmo e ajudam no desenvolvimento e manuteção do código como nesting, mixing, herança, … 

Para usar o sass primeiro usamos o npm para baixar o pacote do mesmo de forma global

```jsx
npm i -g sass
```

Depois usamos este comando onde passamos as flags um arquivo scss para ser compilado em um outro arquivo css

```jsx
sass --watch input.scss output.css
```

## SASS vs SCSS

A única diferença entre um arquivo sass e um arquivo scss é a sintaxe, enquanto o sass tem uma sintaxe mais única o scss tenta replicar o padrão do html e css, em um arquivo scss a heraça é definida por chaves enquanto no sass é definido por indentação, no scss devemos usar ; ao fim de cada linha, no sass não.

## Nesting

Para deixar a leitura do código mais simples o sass estabelece uma hierarquia visual utilizando das chaves, aqui um exemplo:

```scss
// SCSS
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

```css

// CSS

nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```

[BEM ( Block, Element, Modifier )](SASS%20a22ffb5a8b0341679d421b49dfdfd1cd/BEM%20(%20Block,%20Element,%20Modifier%20)%206c62ff4a7b3c4b96a0f240334b7a9078.md)