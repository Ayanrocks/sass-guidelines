
# Too Long; Didn't read

Esta guía es bastante larga y algunas veces es bueno tenerla resumida es una versión más corta. Tienes este resumen a continuación.

## Principios fundamentales

* Tener una guía de estilo es sobre todo tener **consistencia**. Si no estás de acuerdo con algunas reglas de Sass Guidelines, me parece justo, siempre y cuando seas consistente. [↩](#por-qu-una-gua-de-estilo)
* Sass debe permanecer siempre tan simple como se pueda. Evita utilizar sistemas complejos a no ser que sea absolutamente necesario. [↩](#principios-fundamentales)
* Recuerda que algunas veces *KISS* (Keep It Simple, Stupid) es mejor que *DRY* (Don’t Repeat Yourself). [↩](#principios-fundamentales)

## Sintaxis y formato

* La sangría debe hacerse con (2) espacios, no con tabulaciones. [↩](#sintaxis-y-formato)
* Las líneas, deben ser, en la medida de lo posible, más cortas de 80 caracteres. Siéntete libre de dividirlas en disitintas líneas cuando sea necesario. [↩](#sintaxis-y-formato)
* CSS debe escribirse adecuadamente, posiblemente siguiendo la [guía CSS](http://cssguidelin.es) de Harry Roberts. [↩](#sintaxis-y-formato)
* Los espacios en blanco son gratuitos, úsalos para separar elementos, reglas y declaraciones. No dudes en dejar líneas en blanco, no hacen daño. [↩](#sintaxis-y-formato)

### Cadenas

* Declarar la directiva `@charset` al inicio de tu hoja de estilo es altamente recomendable. [↩](#codificacin)
* A menos que se apliquen como identificadores CSS, las cadenas deben ir entre comillas simples. Las URL también deben estar entre comillas. [↩](#cadenas-como-valores-css)

### Números

* Sass no tiene distinciones entre números, números enteros o decimales, por lo que los ceros finales (0) deben omitirse. Sin embargo, los ceros principales (0) ayudan a la lectura y deben agregarse. [↩](#ceros)
* Una longitud cero (0) no debe llevar su unidad. [↩](#unidades)
* La manipulación de unidades debe ser pensada como operaciones aritméticas, no como operaciones entre cadenas. [↩](#unidades)
* Para mejorar la legibilidad, los cálculos de nivel superior se deben incluir entre paréntesis. Además, las operaciones matemáticas complejas podrían dividirse en trozos más pequeños. [↩](#clculos)
* Los números mágicos resultan dramáticamente dañinos para la mantenibilidad del código y deben evitarse en todo momento. En caso de duda, explicar ampliamente el valor en cuestión. [↩](#nmeros-mgicos)

### Colores

* Los colores deben estar expresados en HSL siempre que sea posible, luego en RGB, luego en hexadecimal (en minúscula y en forma corta). Las palabras clave de color deben evitarse. [↩](#formatos-de-color)
* Prefiere `mix(..)` en lugar de `darken(..)` y `lighten(..)` al aclarar u oscurecer un color. [↩](#aclarando-y-oscureciendo-colores)

### Listas

* A menos que se utilice como una asignación directa a valores CSS separados con espacios, las listas deben separarse con comas. [↩](#listas)
* Los paréntesis también se pueden usar para mejorar la legibilidad. [↩](#listas)
* Las listas en una misma línea no deben tener una coma al final, las de varias líneas deben tenerlo. [↩](#listas)

### Mapas

* Los mapas que contienen más de un par clave/valor deben escribirse en varias líneas. [↩](#mapas)
* Para ayudar a la mantenibilidad, el último par de un mapa debe tener una coma al final. [↩](#mapas)
* Las claves de mapa que resultan ser cadenas deben ir entre comillas como cualquier otra cadena. [↩](#mapas)

### Clasificación De Declaraciones

* El sistema usado para clasificar las declaraciones (alfabético, por tipo, etc.) no importa, siempre y cuando sea coherente. [↩](#clasificacin-de-declaraciones)

### Anidamiento de selectores

* Evita anidar selectores cuando no sea necesario (lo que representa a la mayoría de los casos). [↩](#anidamiento-de-selectores)
* Usa el anidamiento de selectores para pseudo-clases y pseudo-elementos. [↩](#anidamiento-de-selectores)
* Las media queries también se pueden anidar dentro de su selector relevante. [↩](#anidamiento-de-selectores)

## Convenciones De Nomenclatura

* Lo mejor es usar las mismas convenciones de nomenclatura CSS que están (excepto algunos errores) en minúsculas y delimitadas por guiones. [↩](#convenciones-de-nomenclatura)

## Comentarios

* CSS es un lenguaje complicado; no dudes en escribir extensos comentarios sobre las cosas que parecen (o son) complejas. [↩](#comentarios)
* Para variables, funciones, *mixins* y *placeholders* que establecen una API pública, usa los comentarios de SassDoc. [↩](#documentacin)

## Variables

* Usa el flag `!default` para cualquier variable de una API pública. Así puede ser cambiada sin generar problemas. [↩](#el-flag-default)
* No uses el flag `!global` a nivel raiz ya que puede considerarse una violación de la sintaxis de Sass en el futuro. [↩](#el-flag-global)

## Extend

* Solo se extienden los *placeholders*, no los selectores existentes. [↩](#extend)
* Extiende un *placeholder* tan pocas veces como sea posible con el finde de evitar efectos secundarios. [↩](#extend)

