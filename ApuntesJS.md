# Apuntes sobre Javascript

## Dia 1 

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
