Recomendador de Películas

Carga de Librerías

En esta sección se cargan todas las librerías necesarias para la implementación del 
recomendador de películas. Las librerías incluyen tanto herramientas de manipulación 
de datos como aquellas especializadas en deep learning para construir y entrenar el 
modelo.

Obtener Datos

Podemos ver cómo es la estructura base de nuestro conjunto de usuarios, donde 
disponemos de rangos de edad, sexo, ocupación y código postal informado. Estos 
datos nos ayudarán a personalizar las recomendaciones y a entender mejor el 
comportamiento de los usuarios.

Exploración de Datos

En esta fase, se lleva a cabo un análisis exploratorio de los datos para comprender la 
distribución de las características y detectar posibles problemas, como datos faltantes o 
distribuciones desbalanceadas, que puedan afectar el rendimiento del modelo.

Ítems (Películas)

Las películas serán los ítems a recomendar a nuestros usuarios. Obtendremos los 
datos del conjunto base y además complementaremos aquella información que 
enriquezca nuestro conocimiento sobre estas películas para recomendar aquellas que 
sean del agrado de nuestros usuarios.

Podemos ver que el conjunto base ya contiene el etiquetado de los géneros de cada 
película en formato OneHotEncoding. Es una forma sencilla de codificar variables 
categóricas de forma que podamos utilizarlas de manera numérica en nuestro modelo.
Veamos ahora cuál es la distribución de nuestros géneros y qué tan balanceado está el 
dataset.

Creación del Modelo de Recomendación

Utilizamos un enfoque basado en deep learning para la creación del recomendador de 
películas. Para ello, empleamos una red neuronal que recibe como entrada las 
características de los usuarios y las películas, y aprende a predecir la probabilidad de 
que un usuario disfrute una película en particular.

El modelo fue construido utilizando TensorFlow y Keras, aprovechando la flexibilidad de 
estas librerías para crear arquitecturas personalizadas. En particular, utilizamos capas 
de embedding para representar tanto a los usuarios como a las películas en un espacio 
de características latente, permitiendo capturar similitudes complejas entre usuarios e 
ítems.

Entrenamiento del Modelo

El entrenamiento se realiza utilizando un conjunto de datos de entrenamiento, donde 
cada entrada está compuesta por un usuario, una película, y la calificación 
correspondiente. Utilizamos la función de pérdida de entropía cruzada para optimizar la 
capacidad del modelo de predecir si un usuario calificaría positivamente una película.
La validación del modelo se lleva a cabo con un conjunto de validación separado, y se 
monitorean métricas como la precisión y el recall para evaluar el rendimiento.

Evaluación del Modelo

Para evaluar el rendimiento del recomendador, se realizó un análisis visual de las 
recomendaciones generadas y se compararon con las preferencias reales de los 
usuarios. Además, se llevó a cabo una evaluación cualitativa para determinar si el 
modelo proporcionaba recomendaciones relevantes y útiles.

Conclusiones y Próximos Pasos

El recomendador de películas basado en deep learning ha mostrado resultados 
prometedores al capturar patrones complejos de preferencias de los usuarios. Sin 
embargo, es importante seguir optimizando el modelo y considerar la integración de 
datos adicionales, como el análisis de sentimientos de reseñas de películas, para 
mejorar aún más la calidad de las recomendaciones
