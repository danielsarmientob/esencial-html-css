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

### Background
  - background-image: linear-gradient(to top, rgba(255,255,255,.3), transparent), url('../images/pattern.png'); -> Permite hacer background multiples de imagenes.
    - linear-gradient(to top, rgba(255,255,255,.3), transparent)
      - to top: De abajo hacia arriba.
      - rgba(255,255,255,.3): Primer color.
      - transparent: Segundo color.
  - background: url('../images/pattern.png');
  - background-repeat: no-repeat;
  - background-position: left 20px bottom -20px;
  - background-size: cover;
 
### Pseudo elementos
  - ::before -> Se agrega un elemento antes del elemento seleccionado.
    - display: inline.
  - ::after -> Se agrega un elemento después del elemento seleccionado.
    - display: inline.
  - ::selecion -> Cambia de color al seleccionar un texto.
    - ```
      ::selection {
          background: red;
      }
      ```
      
### Counters
  - ```
      .section-content {
          counter-reset: titleList; /* La variable titleList se va a resetear para cada div que tenga la clase "section-content" */
      }
      .section-content h3 {
          counter-increment: titleList; /* La variable titleList se va a incrementar para cada h3 que esten dentro de la clase "section-content" */
      }
      .section-content h3::before {
          content: counter(titleList, decimal)". "; /* titleList es la varible para contar y se concatena ". " al número */
      }

    ```
  - listas personalizadas: [https://www.w3.org/TR/CSS2/generate.html#counter-styles](https://www.w3.org/TR/CSS2/generate.html#counter-styles "www.w3.org")

### Wrapper
  - ```
    /* Componente main, pintar fondo */
    main {
    border: 1px solid blue;
    }
    /* Centra el contenido, colocar ancho, dilimitar fronteras */
    .wrapper {
        width: 902px;
        margin: auto;
    }
    /* Contenido del componente main */
    .main-content {
        background: white;
    }
    ```
## Maquetación con propiedades y valores lógicos
### Márgenes
  - ```
    margin-inline: 100px; 
    margin-block: 100px; 
    margin-block-start: 50px;
    margin-block-end: 50px; 
    inline-size: 902px; /* ancho */
    ```
  - Tamaños / wrapper -> Hacer un Scroller
    - ```
      .wrapper {
          border: 1px solid yellow;
          inline-size: 902px; /* ancho */
          block-size: 100px;  /* damos un tamaño pequeño */
          overflow: auto;     /* hacemos que aparezca el scrollo */
          margin: auto;
      }

      ```
### Bordes
  - Página para ver que tecnología esta soportada en los navegadores: [https://caniuse.com/](https://caniuse.com/ "caniuse.com")
  - bordes
    - ```
      pre {
          /* border-left: 5px solid red; */
          border-inline-start: 5px solid white;
          border-inline-end: 5px solid white;
          border-block-start: 10px solid pink;
          border-block-end: 10px solid pink;
          border-block-start-color: 1px solid #5551FF; 
          margin-block-end: 30px;
          /* border-start-start-radius: 60px; */
      }
      ```
  - Sombra 
    - ```
      .sombra {
        /* Sombra: 
            -10px para el eje x
            10px para el eje y 
            0 difuminado
            0 de exprep o cuanto se expande
            #ABBAF6 color 
        */
        box-shadow: -10px 10px 0 0 #ABBAF6;
      }
      ```
  - Modal
    - ```
      .Modal {
          background: red;
          position: fixed;
          inset:0;
          margin-inline: 50px;
      }
      ```
 - Posiciones
    - ```
      header {
          position:absolute;
          /* top */
          inset-inline-start: -188px;
          inline-size: 188px;
      }      
      ```