# CSS-y-Modelo-de-Caja
3. Auditoría manual y corrección del CSS

Al revisar el código CSS proporcionado, encontré tres errores principales.

Error 1: Falta la unidad de medida

El código original tenía:

width: 300;

El problema es que 300 no indica qué unidad se está utilizando. Lo corregí de la siguiente manera:

width: 300px;

De esta forma, la tarjeta tendrá un ancho de 300 píxeles.

Error 2: Falta el punto y coma

En la propiedad del borde se encontraba:

border-style: solid

La corregí agregando el punto y coma:

border-style: solid;

Esto permite mantener correctamente terminada la declaración CSS.

Error 3: Valor incorrecto en text-align

El código original tenía:

text-align: centro;

El valor centro no es un valor válido de CSS para esta propiedad. Lo corregí por:

text-align: center;

Por lo tanto, los tres errores que encontré fueron:

Falta de px en width: 300.
Falta del punto y coma en border-style: solid.
Uso incorrecto de centro en text-align.

El documento indica precisamente que se deben identificar tres errores relacionados con unidades, punto y coma o propiedades/valores escritos incorrectamente.

4. Investigación sobre font-family

Para realizar la investigación consulté la documentación de MDN Web Docs sobre la propiedad font-family.

Las familias tipográficas genéricas principales incluyen:

serif
sans-serif
monospace
cursive
fantasy

MDN explica que serif utiliza pequeños trazos o remates en los extremos de las letras, mientras que sans-serif no utiliza esos remates.

Diferencia entre serif y sans-serif

Serif:
Las letras tienen pequeños remates en sus extremos. Su apariencia puede ser más tradicional o formal.

Sans-serif:
Las letras no tienen esos remates y presentan una apariencia más sencilla y limpia.

Para una página web recomendaría utilizar sans-serif, porque considero que su apariencia es más limpia y facilita la lectura del contenido en una pantalla digital. MDN también señala sans-serif como una opción apropiada para párrafos grandes.

5. Reto del Modelo de Caja

El problema de la tarjeta es que el texto queda demasiado cerca del borde.

Para solucionar este problema se debe utilizar la propiedad:

padding

La razón es que padding crea espacio dentro de la caja, entre el contenido y el borde. En cambio, margin crea espacio fuera de la caja.

Por eso agregué:

padding: 20px;

Mi código corregido para la tarjeta queda de esta manera:

.tarjeta-pokemon {
    background-color: darkred;
    color: white;
    width: 300px;
    margin: 20px;
    border-width: 2px;
    border-color: black;
    border-style: solid;
    padding: 20px;
}

Con esta modificación el texto deja de estar pegado directamente al borde de la tarjeta.

El documento solicita específicamente utilizar padding para crear espacio entre el texto y el borde.

6. Conclusión

Al realizar esta práctica pude comprender mejor cómo funciona CSS y cómo se utiliza el Modelo de Caja para controlar la distribución de los elementos de una página web. También aprendí que propiedades como margin, padding, border, width y font-family permiten controlar diferentes aspectos visuales de una tarjeta.

Considero importante mantener separado el contenido del diseño utilizando un archivo HTML y un archivo CSS externo, porque esto permite tener un código más ordenado, fácil de modificar y mantener. De esta manera, el HTML se encarga principalmente de la estructura y el CSS de la presentación visual. El propio objetivo de la actividad plantea comprender CSS, el Modelo de Caja y documentar las correcciones mediante GitHub y README.md.
