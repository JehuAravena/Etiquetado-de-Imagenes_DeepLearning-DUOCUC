# Proyecto Final - Etiquetado de Imágenes para el Gobierno de Chile

## *Ramo de Deep Learning - DUOC UC (7mo Semestre)*

Este repositorio contiene el código y los modelos utilizados en el proyecto de implementación de inteligencia artificial para el etiquetado de imágenes en la página web del Gobierno de Chile. El objetivo principal del proyecto es seleccionar y clasificar imágenes, detectar objetos, estados de ánimo y rostros utilizando técnicas de inteligencia artificial, como el Aprendizaje Automático. Para obtener más información sobre el proyecto y los detalles de la evaluación, por favor revise el documento de la evaluación llamado "EVALUACIÓN 3 DLY0100 Forma C.pdf".

## Descripción general del proyecto

El Gobierno de Chile busca implementar inteligencia artificial en su página web mediante el etiquetado de imágenes de distintos dominios. Para lograr esto, se utilizan técnicas de Aprendizaje Automático, en particular el Aprendizaje Activo, que mejora la precisión y el rendimiento de los modelos de predicción. En este caso, se emplea el conjunto de datos CIFAR-10, que consta de 60,000 imágenes en color de 32x32 píxeles, distribuidas en 10 clases con 6,000 imágenes por clase.

## Comprensión de los datos

El conjunto de datos CIFAR-10 contiene imágenes etiquetadas de baja resolución. Cada imagen tiene una resolución de 32x32 píxeles y tres canales de color (RGB). Las imágenes están distribuidas en 10 clases, como venado, caballo, camión, rana, avión, gato, perro, pájaro, auto y barco.

## Modelos utilizados

Se han realizado varias pruebas y experimentos para abordar el problema de clasificación de imágenes, y se ha seleccionado el siguiente modelo como el más efectivo para la entrega final:

**Modelo 7:**

El Modelo 7 es una red neuronal convolucional que consta de varias capas para la extracción y procesamiento de características de imágenes. Resumiendo su arquitectura:

- Capas de convolución: Se aplican varias convoluciones a las imágenes de entrada para detectar características relevantes.
- Capas de normalización por lotes: Normalizan las activaciones de las capas anteriores para estabilizar el proceso de entrenamiento.
- Capas de agrupamiento máximo: Reducen la dimensionalidad de las características extraídas mediante el agrupamiento de valores máximos.
- Capas de dropout: Aplican una técnica de regularización que desactiva aleatoriamente un porcentaje de las neuronas durante el entrenamiento para evitar el sobreajuste.
- Capa de aplanamiento: Transforma las características extraídas en un vector unidimensional.
- Capa oculta: Contiene neuronas con una función de activación ReLU y una regularización de tipo L2 para aprender patrones más complejos.
- Capa de salida: Contiene neuronas sin función de activación para clasificar las imágenes en las 10 categorías deseadas.

Este modelo ha demostrado un buen rendimiento en la clasificación de imágenes en el conjunto de datos CIFAR-10. Los detalles completos sobre la cantidad de filtros, tamaños de ventanas y otros hiperparámetros se pueden encontrar en el código fuente.

## Evaluación y resultados

La evaluación de los modelos se basa en la evolución de la pérdida durante el entrenamiento. Se presentan gráficos que muestran la pérdida en el conjunto de entrenamiento y en el conjunto de prueba (validación). Los resultados proporcionan información sobre el rendimiento y la capacidad de generalización de los modelos.

## Requisitos

### Google Colab (No es necesario instalar nada)

Si estás utilizando Google Colab, no es necesario instalar ninguna biblioteca adicional. Solo necesitas subir el archivo .ipynb a Google Colab y seguir las instrucciones del notebook para ejecutar el código.

### Requisitos locales (No se ha probado)

Si prefieres ejecutar el proyecto en tu entorno local, asegúrate de tener instalado lo siguiente:

- Python 3.10.12 (Se recomienda utilizar un entorno virtual)
- Bibliotecas de Python:
  - TensorFlow (``pip install tensorflow``)
  - Keras (``pip install keras``)
  - NumPy (``pip install numpy``)
  - Matplotlib (``pip install matplotlib``)
  - Seaborn (``pip install seaborn``)
  - PIL (``pip install pillow``)
  - Colab (``pip install colab``) - Solo si deseas utilizar la biblioteca Colab para cargar archivos desde tu entorno local.

Es importante destacar que estos requisitos locales no han sido probados, ya que el proyecto se desarrolló en el entorno de Google Colab. Se recomienda seguir la sección de Google Colab para una ejecución sin problemas.

## Contribuciones

Las contribuciones a este proyecto son bienvenidas. Si desea contribuir, siga los siguientes pasos:

1. Realice un fork de este repositorio.
2. Cree una rama nueva para su función o corrección de errores.
3. Implemente los cambios y realice las pruebas necesarias.
4. Envíe una solicitud de extracción a la rama principal.

## Autores

Este proyecto fue desarrollado por los estudiantes de DUOC UC:

- Jehu Elías Aravena Retamales
- Nicolás Montecinos Osses

## Agradecimientos

Queremos expresar nuestro agradecimiento a las siguientes personas e instituciones por su contribución y apoyo en el desarrollo de este proyecto:

- A DUOC por brindarnos la oportunidad de cursar el ramo, incluso cuando nuestra sede no lo ofrecía inicialmente. Su compromiso con la formación de los estudiantes ha sido fundamental para nuestro aprendizaje.
- Al profesor Alvaro Ignacio Torres Mendoza por su dedicación y disposición para aclarar nuestras dudas, incluso fuera del horario de clases y durante los fines de semana. Su guía y conocimiento han sido invaluables para el éxito de este proyecto.

Agradecemos profundamente a todos los mencionados por su valioso apoyo, el cual ha sido crucial en nuestro camino de aprendizaje y desarrollo profesional.
