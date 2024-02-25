# Modelos y Aprendizaje
## Examen
### Planteamiento
Supongamos que usted trabaja en el servicio de salud y recibe muestras que provienen de mujeres con cáncer de mama.

Los médicos han extraído características y las han anotado, su trabajo es crear un modelo que sea capaz de identificar si un paciente tiene o no cáncer.

Recordemos que un falso positivo no es tan preocupante como un falso negativo, ya que en el futuro se le hacen más pruebas a las pacientes y hay oportunidades de descubrir que estábamos en un error.

Sin embargo, un falso negativo puede llevar a que el cáncer se desarrolle sin supervisión durante más tiempo del necesario y podría llevar a daños más graves o incluso la muerte de la paciente.

Teniendo esto en cuenta, desarrolla un modelo que funcione lo mejor posible y explica qué decisiones has tomado en su elaboración y por que.

### Desarrollo

Para el desarrollo del ejercicio propuesto, primero se importaron las librerias necesarias para analizar el data set de Cáncer de mama, incluyendose según se va necesitando.

Se visualizaron los datos de la base de datos cargada, por lo que se decidió aplicar un Análisis de componentes principales (PCA).

Se realizó un grafico de dispersión para visualizar los datos, luego de aplicado el PCA, se estandarizaron los datos para poder trabajar con los modelos de aprendizaje.

Los modelos escogidos para trabajar en el análisis de este data set fueron:
- Regresión Logística
- KNN
- Random Forest

Se trabajó en Test y Train para observar sus resultados de precisión, en base a los resultados de las matrices de confusión y de los resultados de las predicciones.

### Conlusión

**REGRESIÓN LOGÍSTICA**

Regresión logística al ser un modelo de aprendizaje supervisado utilizado para la clasificación binaria, predeciendo la probabilidad de que una observación pertenezca a una de dos clases distintas, en lugar de predecir valores continuos como en la regresión lineal, la regresión logística se utiliza para problemas de clasificación.

Por ende en el contexto de la detección de cáncer, esto es útil para entender el riesgo de que un paciente tenga o no cáncer. Además que el modelo proporciona resultados en términos de probabilidades, permitiendo evaluar el riesgo asociado con cada predicción.

Otra caracteristica es que la regresión logística puede regularizarse para evitar el sobreajuste, siendo útil cuando se trabaja con conjuntos de datos grandes o complejos, donde podría haber muchas características, algunas de las cuales pueden no ser relevantes para la predicción.

**KNN**

KNN (K-Nearest Neighbors / Vecino más cercano), al ser un modelo de aprendizaje supervisado es utilizado para clasificación y regresión. Es uno de los algoritmos más simples y fácil de entender en el campo del aprendizaje automático.

El hiperparámetro k en KNN controla la cantidad de vecinos considerados para la predicción. Esto permite ajustar la sensibilidad del modelo, con valores bajos de k que pueden capturar patrones locales más detallados y valores altos que pueden suavizar el modelo.

Por lo que, para el analisis del data set de cancer de mama, ofrece una alternativa simple y efectiva, especialmente cuando se valora la simplicidad, la no linealidad y la interpretación sencilla de las predicciones, tomando en cuenta que se puede analizar resultados dependiendo de la variable k que se puede encontrar en cada predicción y poder hacer una comparativa con los resultados de la implementación con los otros modelos.

**RANDOM FOREST**

Random Forest al ser un modelo de aprendizaje automático que se utiliza tanto para problemas de clasificación como de regresión. Es una técnica de ensamblado que combina múltiples árboles de decisión entrenados en diferentes subconjuntos aleatorios del conjunto de datos de entrenamiento.

Es por esto que se considero para el análisis del data set de cáncer de mama ya que combina múltiples árboles de decisión para capturar relaciones complejas, lo que suele resultar en una alta precisión en la predicción, tomando en cuenta la naturaleza de los datos del data set y lo importante que resulta reducir los falsos negativos.

### Interpretación de resultados 

Los resultados que se botuvieron con una muestra de:

Datos en Test: 455
Datos en Train: 114

La escala de las mejores predicciones de los 3 modelos considerados para el análisis del data set de Cáncer de mama en Test y Train son:

1)  Random Forest en Train con una predicción de 100%
- Del total de 114 datos, no tuvo errores en las predicciones

2) Regresión Logística en Train con una predicción del 98.6%
- Del total de 114 datos, tuvo error en las predicciones de 4 Benignos que en realidad son Malignos y 2 Malignos que en realidad son Benignos

3) KNN en Train con una predicción de 98.4%
- Del total de 114 datos, tuvo error en las predicciones de 3 Benignos que en realidad son Malignos y 2 Malignos que en realidad son Benignos

4) Regresión Logística en Test con una predicción del 98.2%
- Del total de 455 datos, tuvo error en las predicciones de 2 Benignos que en realidad son Malignos

5) Random Forest en Test con una predicción del 96.4%   
- Del total de 455 datos, tuvo error en las predicciones de 3 Benignos que en realidad son Malignos y 1 Maligno que en realidad es Benigno

6) KNN en Test con una predicción de 95.6%
- Del total de 455 datos, tuvo error en las predicciones de 3 Benignos que en realidad son Malignos y 2 Malignos que en realidad son Benignos
