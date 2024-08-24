# BEM ( Block, Element, Modifier )

BEM é uma metodologia CSS (ou convenção de nomenclatura) usada no mundo todo, está metodologia tenta fazer alusão a POO para nomear “entidades” no CSS.

 Cada letra do acrônimo BEM tem sua função específica:

https://en.bem.info/methodology/quick-start/

## B - BLOCK

Um componente, uma funcionalidade que pode ser reusada no HTML.

Exemplos: 

```jsx
header, input, menu, checkbox, card, button, button-login, button-logout
```

Ao criar um bloco não devemos utilizar seletores aninhados nem IDs, também não devemos usar margens e posicionamentos, isso é uma função dos blocos pais.

```scss
// errado
button.button {
	margin: 40px;
}

#button {}
```

```scss
// certo
.button {}

.content__left {
	margin-right: 50px;
}
```

## E -ELEMENT

Uma parte do bloco que não possuí significado sem seu block e está semanticamente atrelada ao mesmo usando dois underscore(__).

 Exemplos:

```jsx
 menu__item, list__item, checkbox__caption, header__title, search-form__button.
```

Para nos acesarmos a um element no scss usamos o operador & para nos referenciar ao seu block.

Exemplos:

```scss
menu {
	&__item {
		display:flex;
	}
		
	&__button {
	}
}
```

## M - MODIFIER

Uma flag em um bloco ou elemento para mudar sua aparência, estado ou comportamento, está atrelada ao mesmo usando um único underscore ( _ ) ou 2 traços ( — ).

Exemplos: 

```sass
_disabled, _highlighted, _checked, _fixed, _size-big, _color-yellow.
```

```sass
search-form {
	&__button {
		&_disabled {
			opacity: 0.4;
		}
	}
}
```

```sass
search-form {
width: 200px;
	&_size-big {
		width: 500px;
	}
}
```