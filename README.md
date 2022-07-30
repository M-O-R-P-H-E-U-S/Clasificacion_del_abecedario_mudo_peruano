#Clasificacion del abcedario mudo peruano

Abstract
-----

Resumen
-----

Introduccion
-----

Ha habido personas sordas en todos los momentos de la historia humana, y en todas partes en que estas han formado una comunidad, una lengua de señas ha surgido.

Se calcula que existen alrededor de 240 lenguajes de señas para el lenguaje hablado en el mundo. El lenguaje de señas es un tipo de lenguaje que utiliza movimientos de manos, expresiones faciales y lenguaje corporal para comunicarse. Lo utilizan las personas sordas y las personas que pueden oír pero no hablar. Pero también lo utilizan algunas personas oyentes, con mayor frecuencia familias y parientes de los sordos, e intérpretes que permiten que los sordos y comunidades más amplias se comuniquen entre sí. SignLanguage es un lenguaje estructurado en el que cada gesto tiene un significado y un código asignado que utiliza el usuario sordo de señas, tiene su propia gramática y estructura. El lenguaje de señas es solo la forma de comunicación para el usuario sordo de señas.

La LSP es una lengua originaria peruana creada por la comunidad sorda en nuestro país. Como con todas las lenguas, a partir de ella se construyen la identidad, la cultura, el conocimiento ancestral, las tradiciones y las prácticas sociales de sus usuarios. 

Por ello el lenguaje de señas entre países y regiones puede diferir en diversas partes de su estructura, el lenguaje de señas peruano (LSP) es diferente al que se usa en Argentina o en Chile.





La conversión de texto a lenguaje de señas se centra principalmente en la comunicación entre la gente común y las personas sordomudas .  Con la ayuda de la ciencia y la tecnología avanzadas, el investigador desarrolla muchas técnicas para que las personas sordas se comuniquen con mucha fluidez. Los lenguajes de señas son los medios básicos de comunicación entre las personas con discapacidad auditiva. Imagine que desea tener una conversación con una persona sorda, entonces el lenguaje de señas tiene varios gestos y lenguajes corporales para transmitir mensajes a diferencia del patrón de habla verbal. Esto ya puede parecer una tarea tediosa, especialmente si no tienes idea de cómo comunicarte usando el lenguaje de señas. Tal es el problema al que se enfrentan millones de personas sordas que no pueden comunicarse e interactuar con personas oyentes. p.ej. sistemas de reconocimiento de texto y gestos. El reconocimiento del lenguaje de señas es muy importante no para el campo de la ingeniería sino también para la sociedad. Por lo tanto, los avances tecnológicos prometen brindar soluciones para que los sordos se comuniquen con la sociedad. Los sistemas de traducción del lenguaje de señas podrán mejorar la comunicación y permitir que la comunidad sorda disfrute de una participación plena en la interacción diaria y el acceso a la información y los servicios. Los lenguajes de señas de todo el mundo utilizan gestos estáticos y dinámicos, expresiones faciales y posturas corporales para la comunicación. A primera vista, como idea, qué difícil podría hacer un conversor de lenguajes de señas. La pérdida de la audición y del habla puede hacer que las personas se aíslen y se sientan solas, lo que afectará aún más su vida social y laboral. Buscar el significado de un signo no es una tarea sencilla. El lenguaje de señas es un gesto de código bien estructurado donde cada gesto tiene un significado asignado. La Lengua de Signos es el único medio de comunicación para las personas sordas. Con el avance de la ciencia y la tecnología se han desarrollado muchas técnicas no solo para minimizar el problema de las personas sordomudas sino también para implementarlo en diferentes campos. El lenguaje de señas es un lenguaje que, en lugar de patrones de voz o sonido, utiliza la comunicación manual y el lenguaje corporal para transmitir el significado. Esto implica principalmente la combinación de formas, orientación y movimiento de las manos. El lenguaje de señas no solo lo usan los sordos, sino también los que pueden oír, pero no pueden hablar físicamente. Toda la Federación India de Sordos estima que alrededor de 4 millones de personas sordas y más de 10 millones de personas tienen problemas de audición en la India. Los estudios dicen que una de cada cinco personas sordas en el mundo es india. De ellos, más de 1,5 millones de sordos


Estado del Arte
-----

Realidad
-----

El Lenguaje de Señas Peruano(LSP) no cuenta con el debido reconocimiento por parte de las políticas públicas. A pesar de ser una lengua oficial(Ley 29535), hasta el momento los textos especializados que listan las lenguas peruanas no la incluyen. 
La educación de la persona sorda en nuestro país está todavía estancada en el viejo paradigma clínico y oralista. Las niñas sordas y los niños sordos en el Perú no reciben oportunamente acceso a la lengua de señas, y quedan así privados de oportunidades valiosas para su desarrollo academico y social, lo que constituye un acto de negligencia que vulnera sus derechos básicos como persona.

Problematica
-----

El Lenguaje de Señas es un lenguaje visual, por ello nuestro proyecto no asimila los siguientes signos: j, ñ, ll, rr, s, z. Signos realizados mediante movimientos de zig-zag o de repeticion, a diferencia de los demas signos que se pueden entender de manera estatica. Debido a su complejidad visual para poder formar parte de nuestro algoritmo de reconocimiento de signos, no son asimilados en nuestro proyecto.   

Metodologia
-----

Para poder construir nuestro dataset, comenzamos grabando nuestra mano ya sea la mano izquierda o la derecha debido a que los signos se interpretan de la misma manera sin importar con que mano se realizan. Grabando cada signo durante 40s siendo 02 videos por signo(02 manos), en total 46 videos de 40s cada uno. 

Creamos las siguientes carpetas: GS_28, GS_50, RGB_28, RGB_50. Carpetas cuya finalidad es 

Seguidamente ordenamos nuestos videos en carpetas con el nombre de las letras del abecedario, cargamos nuestro dataset de videos, definiendo las dimensiones en pixeles que deseamos obtener de los frames de nuestros videos y customizando los canaloes a analisar(RGB y GRAYSCALE), al siguiente script:

```
from_mp4_to_jpg.py
```
Donde se almacenaran los siguientes 
Ordenamos nuestro nuevo dataset de fotos en carpetas con el nombre de las letras del abecedario. 
Cargamos nuestro dataset de fotos,ordenandolos en las filas por etiquetas y en las columnas por pixeles , al siguiente script:

```
convert_to_csv.py
```

Con un tal de 784 columnas para los frames de (28px)x(28px), 2500 columnas para los frames de (50px)x(50px) en escalas de grises. Y en los 03 canales(RGB) 2352 columnas para los frames de (28px)x(28px), 7500 columnas para los frames de (50px)x(50px).

Ahora que tenemos nuestro dataset en archivos csv,mezclaremos las filas con susrespectivas etiquetas para ser mas dinamico el aprendizaje de nuestro modelo.
Para ello cargaremos nuestro dataset de archivos csv al siguiente script:

```
shuffle.py
```


```
from_mp4_to_jpg.py
```
```
Ploting_images.py
```

Experimental
-----



Resultados
-----


Conclusiones
-----

Trabajos Futuros
-----

El presente proyecto traza el camino para poder desarrollar un algoritmo mas sofisticado que cuente con un dataset mas robusto, donde se pueda facilitar la comunicacion entre las personas no sordomudas y las personas sordomudas.
