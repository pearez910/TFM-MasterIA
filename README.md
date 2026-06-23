# TFM-MasterIA

Proyecto de trabajo de fin de máster centrado en análisis de datos y experimentación con inteligencia artificial.
El proyecto comienza con la premisa que en la actualidad existen muchos usuarios de smartwatches que usan aplicaciones de entrenamiento
que generan unas cantidades masivas de datos. Estos datos no etiquetados pueden servir entre muichas otras cosas a clasificar a los usuarios de estas aplicaciones en distintos perfiles en funcion de los datos obtenidos. Gracias a estos perfiles se podrian ofrecer a los usuarios clasificados, planes de entrenamientos mejor ajustados a sus caracteristicas fisiologicas de esta manera, se podria mejorar su rendimiento y capacidades fisiologicas de una manera mas efectiva.
Para el experimento se ha utilizado el data set de Endomondo, el cual parte de mediciones realizadas por smartwatches en mas de 11.000 sesiones de entrenamientos de runnig.
Durante el desarrollo del experimento se han utilizado tres algoritmos de aprendizaje automatico no supervisado:
- K-means
- DBSCAN
- Clustering Jerarquico
Como resultado final del experimento, tras analizar los distintos modelos, el mejor output y metricas ha sido K-means. Este con un k=9 ha conseguido hacer una division efectiva del dataset en 9 perfiles de corredor muy diferenciados entre ellos.
Con este experimento se muestra una solucion escalable y valida para la generacion de perfiles a partir de datos recogidos por smartwatches.

## Contenido

- `main.ipynb`: Notebook principal con el desarrollo y los análisis.

## Uso

1. Abrir el notebook `main.ipynb` en Jupyter Notebook o JupyterLab.
2. Ejecutar las celdas en orden para reproducir el análisis.

## Nota

Este repositorio es una versión de trabajo del proyecto y puede necesitar datos adicionales o dependencias específicas para ejecutarse correctamente.