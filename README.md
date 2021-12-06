# W7-Kaggle-Competition-DaniHelguera

En este proyecto se busca obtener un modelo de regresión con la mayor precisión posible.

### Pasos
Basicamente dos ficheros:
    a) EDA y limpieza de datos
        -   EDA
        -   limpieza de duplicados,
        -   limpieza de Nulls, NaNs y valores no válidos
        -   análisis variables categoricas
        -   análisis variables numéricas
        -   limpieza de outliers
        -   normalización de la variable objetivo
        -   análisis multicolinearidad
        -   grafico variable objetivo en funcion de predictores (scatterplot)
        -   grafico variable objetivo transformada (logaritmica) en funcion de predictores (scatterplot)
        -   Codificación numérica de variables categóricas
        -   exportación de CSV
    
    b) Iteración de regresiones
        -   Generación subsets train y test
        -   Normalización de variables numéricas (escalar y polinómica)
        -   Codificación numérica de variables categóricas
        -   Entrenamiento supervisado de diferentes modelos de regresión
        -   Cálculo de metricas para cada modelo de regresión
        -   Selección de modelo benchmark y optimización hiperparámetros (GridSearchCV)
        -   Entrenamiento supervisado modelo regresión benchmark optimizado
        -   Predicción de objetivo con modelo benchmark optimizado
        -   Submission de predicción en Kaggle

### Resultados
El mejor resultado lo ha conseguido el modelo LGBMReg, con una RMSE de 527. 
Después de la optimización de hiperparámetros, se ha bajado la RMSE hasta 515.

En cuanto a la codificación, normalización y estandarización de resultado:
    Variables categoricas: el mejor resultado se ha obtenido con OneHotEncoder frente a LabelEncoder
    Variables numéricas: el mejor resultado se ha obtenido con una estandarización de los datos en vez de con los datos sin escalar
    Variable objetivo: el mejor resultado se ha obtenido usando la transformada logaritmica del objetivo frente a la variable no transformada

A pesar de la alta colinearidad de varios predictores numéricos, el entrenamiento de los modelos quitando dichos predictores colineares no mejora el RMSE, aunqué sí reduce significativamente el tiempo de computación.

Otros modelos con muy buenos resultados son Random Forest Regressor, Extra Trees Regressor y XGB Regressor.

### Tecnologia
Aparte de las típicas librerías Pandas, Numpy, Matplotlib, Seaborn y time, en este proyecto se exploran sobretodo las librerías:
    - sklearn
    - scipy
    - lightgm
    - xgboost


