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


### Funciones:

* `repeat(cantidad, valor)` para usar el mismo valor varias veces.  

* `minmax(min, max)` agregar un valor minimo y maximo para el tamaño al hacer responsive.
