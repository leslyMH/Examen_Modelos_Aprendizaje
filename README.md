# Examen_Modelos_Aprendizaje
## Modelos y Aprendizaje
### Examen
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
