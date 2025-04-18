# Apuntes sobre Javascript

## Dia 1 - HTML

URL = Uniform Resource Locator y al activar una url como:

http://www.google.com estoy diciendo:

Utiliza el protocolo http, para acceder a la world wide web google.com, luego recibimos instrucciones, estas instrucciones son de tres tipos HTML (estructura), CSS (estilo), Javascript (comportamiento)

###HTML

Es para dar estructura, es un lenguaje de marcación , Lenguaje de Marcas de HiperTexto

Siempre empieza por <!DOCTYPE html>  y termina con </html>, y el código dentro de esas etiquetas se divide en:
1. Head: <head> </head> Tiene el título, estilo y comportamiento
2. Body: </body> </body> Todos los elementos del sitio y suele ser más extenso

#### Etiquetas HTML de Estilo de Texto

1. Énfasis / Cursiva
- `<em>` – Énfasis (semántico, accesible)
- `<i>` – Cursiva (solo visual)

> 🔹 Ambas se ven parecidas (cursiva), pero `<em>` tiene más significado semántico.

2. Negrita / Importancia
- `<strong>` – Énfasis fuerte (semántico, accesible)
- `<b>` – Negrita (solo visual)

> 🔹 Ambas se ven en negrita, pero `<strong>` indica importancia real en el contenido.

3. Texto pequeño
- `<small>` – Reduce el tamaño del texto


4. Texto tachado
- `<del>` – Texto eliminado o tachado


5. Texto insertado / subrayado
- `<ins>` – Texto insertado (subrayado semántico)
- `<u>` – Subrayado (visual solamente)

> 🔹 Ambas generan subrayado, pero `<ins>` tiene un propósito semántico (por ejemplo, en documentos editados).

6. Texto resaltado
- `<mark>` – Resalta o marca texto (fondo amarillo por defecto)

#### Etiquetas anidadas
Si fuese necesario se ppueden usar etiquetas anidadas
<b>Hola <i>Mundo</i>, buenos dias</b>

<pre> hace que el texto dentor de estas etiquetas de vea literalmente como esta escrito

<p>Separa parrafos

&lt; &gt;, asi pondriamos poner los simbolos < y >, en google podemos encontrar lso códigos de los simbolos y lo semojis

<!- Asi se ponen los comentarios (falta un guion al principio es !--)  -->

#### Imagenes
Se puede definir como poner en el centro, se ponen con la etiqueta <img>
<img src="nombre del archivo" width="100%" alt="nombrefoto" align="left" hspace="20">
width puede ir en píxeles aunque es mejor ponerla en tamaño porporcional (600 ó 100%)
alt sirve para aparecer en los bsucadores web y esas cosas y que paarezca como texto alternativo
hspace crea un pequeño margen de ese numero de píxeles

## Dia 2 - CSS

El CSS sirve para dar estilo, se suele hacer a través de etiqueetas

<etiquetas style= "Propiedad de estilo: valor">

<p style="color: rgb(0, 0, 0);
            background-color: rgb(42, 226, 233);
             font-family: 'Times New Roman', Times, serif;
             font-size: 1em;
             margin: 20px;
             border:3px;
             border-color: blue;
             padding:10px">

Así definiriamos un estilo en parrafo, esto no se suele hacer así sino que se suele crear un archivo con los estilos separados, Si te fijas en font-family hay muchas familias, esto es debido a que el usuario de la página podría no tner disponible alguna de ellas, entonces el código indica que si no tiene Times New Roman salte a Times, y si no tiene times, salte a Serif.

Font-size 1em es el tamaño normal, 2em es dos veces e, tamaño normal, 3em...

El borde define un cuadrado, separado del texto por el padding, al final definen varios rectangulos concentricos, en este orden margin > border > padding

Para definir el estilo se puede definir en cada parrafo (lo peor) , defini en el head que se vería así:

<style>
    h1{
        font-family: 'cpurier New', Courier, monospace;
        color: red
    }
    p{
        color:verde
    }
</style>

Podríamos volver a definir en un parrafo específico un nuevo estilo, las ordenese más específicas sobrescriben a las menos específicas

Pero el **mejor método** es este, se crea un ahoja de estilo y se le referencia de esta forma

<link rel="stylesheet" href="misestilos.css"> 

y en misestilos.css debería haber algo así (misestiloscss es un nombre genérico apra la hoja de estilos)

h1{
    font-family: 'cpurier New', Courier, monospace;
    color: red
}
p{
    color:verde
}

Se puede aplicar **clases** a los parrafos, para asi auqneu los parrafos compartan la etiqeuta p o h1, lleven estilos diferentes, en la hoja de estios se define como

.nombreclase{
    color:rojo
}

Y en le parrafo se definiria como <p class="nombreclase"> y en el orden de especifidad están por delante de el estilo de p, rollo lo que tu definas sobr elos parrafos de tipo p, se sobrescribe con las clases

Las etiquetas <div> sirven oara agrupar elementos, y se puede definir una clase o estilo para todo ese grupo y <span> hace lo contrario
 
<div class ="nombreclase">
    <p>a+b= <span class="otraclase"> c </span> </p>
    <p>b</p>
    <p>c</p>
</div>

Los grupos de selectores pueden ser de tipo (h1{estilo}) de clase (.nombreclase{estilo}) y ID (#nombreID {estilo})- los de Id solo pueden aplicarse a un elemento por sitio web

Los grupos de elemento por atributo funcionan así

a[href*= ".edu"]{estilo} 

Y sirevn para seleccionar en este caso a todos los elementos que contengan .edu

Los elementos de pseudo-clases y pseudo-elementos, un jemplo sería

p:hover{estilo}

Y en este caso se activria cuando pase el raton por encima de el

p::firstline es un pseudo elemnto y afectaría solo al primer elemento de cada parrafo

Todas estas se definirian en la hoja de estilos.

Otros elementos que no hemos visto son las listas ordenadas o desordenadas (HSS)

Los **combinadores** los hay de varios tipos, descendientes (div), hijos directos (ol>li, se nombramn así y solo afectaría a li, si li tiene hijos no les afecta), hermanos adjacentes (h1+h2, solo afectaran a los h2 que tiene antes un h1), ( hermanos generales (h1~h2)