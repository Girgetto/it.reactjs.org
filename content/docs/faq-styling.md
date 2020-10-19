---
id: faq-styling
title: Stili e CSS
permalink: docs/faq-styling.html
layout: docs
category: FAQ
---

### Come aggiungo classi CSS in un componente? {#how-do-i-add-css-classes-to-components}

Passa una string come una prop `className`:

```jsx
render() {
  return <span className="menu navigation-menu">Menu</span>
}
```

È comune per una classe CSS di dipendere dal componente props o stato:

```jsx
render() {
  let className = 'menu';
  if (this.props.isActive) {
    className += ' menu-active';
  }
  return <span className={className}>Menu</span>
}
```

>Consiglio
>
>Se ti trovi spesso a scrivere codice di questo tipo, il pacchetto [classnames](https://www.npmjs.com/package/classnames#usage-with-reactjs) può semplificarlo.

### Posso utilizzare stili in linea? {#can-i-use-inline-styles}

Si, guarda la documentazione sugli stili [qui](/docs/dom-elements.html#style).

### È sbagliato mettere gli stili in linea? {#are-inline-styles-bad}

Le classe CSS sono generalmente migliori per la performance invece che gli stili in linea.

### Cosa è CSS-in-JS? {#what-is-css-in-js}

"CSS-in-JS" si riferisce a un pattern dove il CSS è composto utilizzando JavaScript invece di definirlo un file esterno.

_Note that this functionality is not a part of React, but provided by third-party libraries._ React does not have an opinion about how styles are defined; if in doubt, a good starting point is to define your styles in a separate `*.css` file as usual and refer to them using [`className`](/docs/dom-elements.html#classname).

_Nota che questa funzionalità non fa parte di React, ma è data da librerie di terzi._ React non opina sul come gli stili sono definiti; se in dubbio, un buon punto di inizio è di definire i tuoi stili in un file separato `*.css` come di normale e riferirsi ad esso utilizzando [`className`](/docs/dom-elements.html#classname).

### Posso fare animazioni in React? {#can-i-do-animations-in-react}

React può essere utilizzata per potenziare animazioni. Guarda [React Transition Group](https://reactcommunity.org/react-transition-group/) e [React Motion](https://github.com/chenglou/react-motion) o [React Spring](https://github.com/react-spring/react-spring), per esempio.
