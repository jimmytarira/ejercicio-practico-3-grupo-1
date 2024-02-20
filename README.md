# ejercicio-practico-3-grupo-1
Ejercicio práctico 3 del Grupo 1 - Fashion MNIST

GRUPO # 1

Integrante:
Jimmy Tarira

Ejercicio sobre el Dataset Mnist Fashion de Zalando

Este Dataset Fashion-MNIST contiene 60.000 imágenes de entrenamiento y 10.000 imágenes de prueba de imágenes de artículos de Zalando.
El conjunto de datos consta de imágenes en escala de grises de tamaño 28x28 píxeles.
Cada píxel tiene asociado un único valor de píxel, que indica la claridad u oscuridad de ese píxel, y los números más altos significan más oscuro. Este valor de píxel es un número entero comprendido entre 0 y 255.

Este Dataset Fashion-MNIST se utiliza ampliamente para entrenar y probar en el campo del aprendizaje automático, especialmente para tareas de clasificación de imágenes.
Con este Dataset se va a realizar el entrenamiento de una red neuronal convolucional con sus siglas CNN para clasificar imágenes de prenda de vestir de 10 categorías.

Este tipo de red contiene diferentes capas:
•	La capa layers.Conv2D(32, kernel_size=(3, 3), activation="relu") realiza una convolución 2D con un filtro de 3x3 y 32 filtros, extrayendo características y reduciendo la dimensionalidad de la imagen.
•	La función de activación "relu" introduce no linealidad en la capa, lo que permite que la red neuronal aprenda relaciones más complejas.

•	La capa layers.MaxPooling2D(pool_size=(2, 2)) reduce la dimensionalidad de la imagen y extrae características robustas.
•	La capa divide la imagen de entrada en regiones no superpuestas.
•	De cada región, se selecciona el valor máximo.
•	Esto reduce la cantidad de datos que la red neuronal necesita procesar.

•	La capa layers.Flatten() toma una entrada de tensor multidimensional y la convierte en un vector unidimensional. En otras palabras, convierte una matriz en una lista.

•	La capa Dropout funciona desactivando aleatoriamente una cierta cantidad de neuronas en la red neuronal durante el entrenamiento.
•	Esto obliga a la red neuronal a aprender a depender de otras neuronas, lo que la hace más robusta y menos propensa a sobreajustarse a los datos de entrenamiento.

•	La capa layers.Dense(num_classes, activation="softmax") se utiliza para clasificar la entrada en una de las num_classes categorías.
•	La función de activación "softmax" se utiliza para convertir los valores de entrada en probabilidades válidas.

El accuracy del train (entrenamiento) fue de 0.9132 es decir el 91.32%, mientras que el del test (evaluación) fue de 0.9053 es decir el 90.53%
En las matrices de confusión del train y del test se puede notar que para 25 épocas no hay tanta diferencia, se escogieron 25 épocas como balance para no hacer tan complejo el modelo, pero que no tengo tanto error tampoco.

Se puede concluir que funciona bien y que permite generalizar, es decir que para imágenes nuevas diferentes a las del conjunto de datos se tiene un alto porcentaje de acierto.
