## Resumen del Curso de CSS Grid Layout

### Conceptos Fundamentales:
>**CSS Grid Layout** contiente funciones de diseño dirigidas a los desarrolladores de aplicaciones web. El CSS grid se puede utilizar para lograr muchos diseños diferentes. Destaca por dividir una página en regiones principales, o definir la relación en términos de tamaño, posición y capas entre partes de un control construido a partir de primitivas HTML.
[MDN](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout)

* **Grid Container:** Es el elemento padre que recibira un display: grid. Recibe otras propiedades para manejar la grid.

* **Grid Line:** Lineas divisorias de manera horizontal y vertical.

* **Grid Track:** Espacio entre dos líneas adyacentes. Filas y columnas.

* **Grid Cell:** Celdas, unidad minima o espacio en dos filas adyacentes y 2 columnas adyacentes.

* **Grid Area:** Espacio contenido por una cuadrícula de celdas

* **Grid explicito (explicit grid):** es cuando nosotros definimos el numero de filas o columnas.

* **Grid implicito (implicit grid):** es cuando tenemos filas o columnas que no definimos pero son parte de nuestro grid.

* **Unidad de medida:** fracciones **(fr)** distribuye el espacio disponible en formas iguales.

## Vamos al codigo

`display: grid` asignamos la grid a nuestro contenedor padre.

`grid-template-columns: parametros` definimos el ancho de cada una de las columnas (separados por espacios), el cual definira nuestro número de columnas.

`grid-template-rows: parametros` definimos el alto de cada unas de las filas (separados por espacios).

`grid-template: filas / columnas` mediante esta propiedad podemos definir filas y columnas de una manera reducida.

`display: subgrid` hereda la configuración del grid padre (cuando se esten anidando grids).
**No disponible aun**.

`display: inline-grid` muestra el grid en una sola linea. **No disponible aun**.

`grid-column-gap: valor`Espaciado entre columnas.

`grid-row-gap: value` Espaciado entre filas.

`grid-gap: filas columnas` Espaciado.

`grid-template-areas: "contenido"` definimos las areas de nuestro grid, se encierran en comillas cada una de las columnas que contiene una fila. Para usar estas areas debemos asignarle a cada elemento un area con la propiedad `grid-area: contenido`.

Definiendo el tamaño de los columnas dentro de un grid

**Para definir el tamaño de las columnas dentro de un grid usamos:**

`grid-column-start: 1;` donde empieza el elemento.

`grid-column-end: 3;` donde termina el elemento.

Para escribir esto en una sola linea:

`grid-column: inicio / final;`

estas propiedades se rigen por las lineas del Grid, pero añadiendo `span` lo tomara por espacios.

**Para definir el tamaño de las filas dentro de un grid usamos:**

`grid-row-start: valor` donde empieza el elemento.

`grid-row-end: valor` donde termina el elemento.

para escribir esto en una sola linea usamos `grid-row: inicio / final`

**Para definir el nombre de las lineas debemos colocar los nombres en corchetes y en medio de cada una de las medidas.
Ejemplo: `grid-template-rows: [start] 1fr [middle] 1fr [end];`**

**Manejando el grid implícito**

Para cambiar el flujo automático de mi grid:

`grid-auto-flow: column;`

Por defecto viene `grid-auto-flow: row;`

Para asignar el valor por defecto de el espacio de las columnas o filas que no han sido asignadas:

`grid-auto-columns: valores;`

`grid-auto-rows: valores;`

### Funciones:

* `repeat(cantidad, valor)` para usar el mismo valor varias veces.  

* `minmax(min, max)` agregar un valor minimo y maximo para el tamaño al hacer responsive.
