Inteligencia Artificial - Universidad de Palermo
Resolución de la actividad numero 09 Redes neuronales convolucionales

Este ejercicio realiza un simple análisis de sentimientos sobre reseñas de películas. Para predecir si una reseña nueva corresponde a una reseña positiva o negativa.
Para explicar mejor el código lo separé en distintas etapas que son:

Etapa 1: Preprocesamiento de los datos
  Carga de datos: Importar las bibliotecas necesarias y cargar un conjunto de datos de reseñas de películas (descargado de Kaggle) en un DataFrame de Pandas.
  Limpieza de datos: Manualmente se eliminaton carachteres inválidos y se hizo una limpieza general del archivo CSV. A nivel de código se eliminan registros inválidos o vacíos del DataFrame.
Etapa 2: Preparación de datos
  División de datos: Divido el conjunto de datos en conjuntos de entrenamiento y prueba.
  Codificación de etiquetas: Se mapean las valoraciones que originalmente son texto a valores numéricos para facilitar el procesamiento por el modelo de aprendizaje. Es decir "positiva" lo mapeamos con 1 y "negativa" con 0.
Etapa 3: Tokenización y secuenciación de texto
  Tokenización: Convierte el texto de las reseñas en secuencias de números utilizando la clase Tokenizer de Keras.
  Alineación de secuencias: Ajusta la longitud de las secuencias de entrada a un tamaño fijo para que todas tengan la misma longitud utilizando el relleno y truncado.
Etapa 4: Construcción y entrenamiento del modelo
  Definición del modelo: Define un modelo de red neuronal secuencial utilizando capas de Embedding y LSTM.
  Compilación del modelo: Configura el modelo para el entrenamiento especificando la función de pérdida y el optimizador.
  Entrenamiento del modelo: Entrena el modelo utilizando los datos de entrenamiento preparados.
Etapa 5: Evaluación del modelo
  Evaluación del rendimiento: Evalúa el rendimiento del modelo utilizando los datos de prueba y calcula su precisión.
  Guardado del modelo: Guarda el modelo entrenado para su uso futuro y no tener que entrenar nuevamente al modelo.
Etapa 6: Uso del modelo entrenado con ejemplos  
  Predicción de sentimiento: Utiliza el modelo entrenado para predecir el sentimiento de una nueva reseña de película. (Una positiva y una negativa).
