# Esencial html, css
## Conceptos esenciales
### Insertar código
  - ``<pre></pre>`` : para insertar un bloque de código.
  - ``<code></code>``: para inserta un línea de códigot.
  - Página para escapar código: [https://www.freeformatter.com/html-escape.html](https://www.freeformatter.com/html-escape.html "freeformatter.com")

### Selectores
  - PseudoClase: es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado, ejemplo: :hover.
    - PseudoClase: [https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes "developer.mozila.org")
  - PseudoElemento: Crea elementos especiales, ::afeter, ::before

### Display/Flujo/Línea y bloque
  - Flow layout
    - writing-mode: horizontal-tb, tb: top to bottom
    - direction: ltr: Horizontal se lee de izquierda(left) a derecha(rigth)
 
## CSS para contenido

### Valores y unidades
  - Por defecto el font-size es de 16px.
  - em: Toma como referencia al padre más cercano que tenga.
  - viewport(v)-> Tamaño de toda de la pantalla ancho y largo.
    - vw -> Ancho de pantalla.
    - vh -> Largo de pantalla.
 - rem: Toma como referencia al padre más alejado que tenga.

### Fuentes personalizadas
  - @font-face: Permite agregar fuentes que se descargan para tu página.
  - font-weight: 400, font-weight: normal-> Ambos indican lo mismo.
