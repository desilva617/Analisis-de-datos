
# Análisis de videojugos, ¿tienen éxito o o no?
## Introducción 
Este proyecto consiste en preparar un informe sobre las reseñas de usuarios y expertos, los géneros, las plataformas (por ejemplo, Xbox o PlayStation) y los datos históricos sobre las ventas de juegos están disponibles en fuentes abiertas. 
El dataset contiene la abreviatura ESRB. The Entertainment Software Rating Board (la Junta de clasificación de software de entretenimiento) que evalúa el contenido de un juego y asigna una clasificación de edad como Adolescente o Adulto.
Se identifica patrones que determinen si un juego tiene éxito o no que servirá para detectar proyectos prometedores y planificar campañas publicitarias.
## Contenido

* [Introducción](#intro)
* [Carga de librerías y datos](#data_review)
* [Exploración de datos](#explore)
* [Preparación de datos](#data_preprocessing)
    * [Reemplazo de los nombres de las columnas](#header_style)
    * [Manejo de datos ausentes](#missing_values)
    * [Corrección en tipo de datos](#duplicates)
    * [Añado de columna](#data_preprocessing_conclusions)
* [Análisis de los datos](#analisis)
    * [Número de juegos lanzados en diferentes años](#1)
    * [Distribución de número de ventas de las plataformas](#2)
    * [Distribución de número de juegos de las plataformas](#3)
    * [Plataformas que antes eran populares y ahora ya no lo son](#4)
    * [Periodo de mayor número de ventas](#5)
    * [Rentabilidad de los juegos por género](#6)

* [Perfil de usuario para cada región](#perfil)
    * [Plataformas principales](#header_style)
    * [Géneros principales](#missing_values)
    * [Ranking vs ventas](#duplicates)
* [Análisis de los datos](#analisis)
    * [Números de juegos lanzados en diferentes años](#header_style)
    * [Periodo de mayor número de ventas](#missing_values)
    * [Rentabilidad de los juegos por género](#duplicates)
* [Prueba de hipótesis](#hypotheses)
    * [Calificaciones promedio de los usuarios para las plataformas Xbox One y PC](#activity)
    * [Calificaciones promedio de los usuarios para los géneros de Acción y Deportes ](#week)
* [Conclusiones](#end)
## Conclusión del proyecto 
En conclusión, se pudo preparar los datos cambiando los datos de algunas columnas al tipo de datos correcto con la función astype(), corrigiendo los nombres de las columnas para que esten en minúsculas con str_lower() y manejando los datos ausentes en la columna tipo categorica reemplazando los NA con strings vacíos, en los numericos no se pudo eliminar los datos ausentes porque los NA eran aleaorios y las filas contenían información importante. También se añadió una columna de las ventas totales que ayudó en todo el proyecto a definir el éxito de los juegos.

Las tablas dinámicas fueron de ayuda para determinar las plataformas principales y la distribución de sus ventas y juegos a través del tiempo. Se pudo determinar los géneros principales, clasificar por región y definir el periodo con la información importante. Las función query() también ayudó para filtrar las tablas juntos con los condicionales y la función merge() para unir tablas y crear dataset más completos.

Se visualizó las plataformas, genéros y clasificaciones principales con gráficos de barras. Los graficos lineales ayudaron a ver la distribución de los juegos y ventas a través del tiempo. La distribución de los datos se vio con el diagrama de cajas. Se utilizó también gráficos de dispersión para visualizar la correlación de las reseñas con las ventas.

Se pudo sacar las siguientes conclusiones: 
- El 2008 y 2009 han sido los años que más juegos se ha lanzado.
- En el periodo 2005 - 2011 se observó el pico más alto en ventas
- El tiempo promedio de vida de las plataformas es de 6 años.
- Las 6 plataformas que representaron un número de ventas significativo fueron la PS2, X360, PS3, Wii, DS y PS.
- Se observó que las ventas de las plataformas con mayores ventas se mantuvieron por un periodo de 4 a 6 años y luego empezaron a decaer.
- Las seis plataformas con más ventas en el periodo  2005 - 2010 fueron Wii, DS, X360, PS3 y PS2 PSP
- Las plataformas empiezan teniendo ventas bajas y en 1 año han tenido resultados favorables, y en un periodo de 2 a 5 años han presentado su pico más alto en ventas. 
- Al vender menos de 100 juegos las plataformas ya está casi muerta 
- Las plataformas que solían ser populares han tardado en desaparecer 9 años en promedio.
- El PS3 y X360 tuvieron tendencia a crecer en subir sus ventas en un periodo de 5 años.
- Al parecer para tener una proyección positiva en ventas, se debe tener un crecimiento de más de 50 millones cada año. 
- Las reseñas de los usuarios con las ventas tienen una muy baja correlación.
- Se observó que los juegos de acción y de deportes son los géneros más rentables
- Las plataformas principales de europa y norteamerica son  Wii, DS, X360.
- Las plataforma DS es la principal en japón.
- Los géneros principales en norteamerica y en europa son acción, deportes, misc y disparos.
- En Japón los juegos de rol son los más populares.
  Las clasificaciones de ESRB si afectan a las ventas en cada región.

Sobre la combrobación de hipótesis:
- Las calificaciones promedio de los usuarios para los géneros de Acción y Deportes son las mismas.
- Las calificaciones promedio de los usuarios para las plataformas Xbox One y PC son diferentes
