# ProyectoU3
## Proyecto de CNN para Fundamentos de Deep Learning
## Mabel Catalina Zapata y Gabriel Maldonado Colmenares
### La tarea que se propuso fue la de *clasificar* un dataset de imágenes compuestas por radiografías de pecho en las cuales 
### se encuentran 2 clases, las cuales son: radiografías de personas normales y radiografías de personas con pneumonia.
Nota: Se utilizo Python 2.7 en un entorno de anaconda para el desarrollo del proyecto.
En primer lugar se debe ejecutar el script *DescargaRecursos.ipynb*, esto descargará las imagenes y los pesos de la red VGG 
mediante un enlace de dropbox.
Ademas en este mismo script se pueden descargar las librerias utilizadas solo de ser necesario.

El repositorio posee 4 versiones:
### U3_Version0:
En este se realiza un primer acercamiento a la clasificación deseada por medio de transfer learning con los
pesos preentrenados de las primeras dos capas del modelo AlexNet, sin embargo con esta arquitectura se encontró un mal desempeño
debido aque que faltaba complejidad, con respecto a las imagenes utilizadas.
### U3_Version1: 
Se plantea la tranferencia de aprendizaje a partir de la red VGG, sin embargo esta version es poco eficiente en 
cuestion de recurso ya que al cargar todas las imagenes observamos que en algunas maquinas se quedaban sin memoria a la hora de entrenar

### U3_Version2:
Este version posee el mejor resultado obtenido, en esta se implementa el entrenamiento utilizando el metodo ImagenDataGenerator 
de Keras lo cual nos permite utilizar un batch mas grande y por lo tanto usamos 3 epocas. Se obtuvieron los resultados y se 
analizaron distintas metricas

### U3_Version3:
Mismo flujo de trabajo que la version 2  (U3_Version2), con la variacion de que se agrego normalizacion a las imagenes, sin
embargo no se obtuvo mejora.

El mejor resultado se obtuvo en el notebook U3_Version2, donde apesar de poseer un leve sobreajuste debido al desbalance de clases
notamos que posee una alta sensibilidad ante las imagenes con neumonia, tanto el los set de testo como validacion.


