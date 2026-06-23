# TFM-MasterIA

Proyecto de trabajo de fin de máster centrado en análisis de datos y experimentación con inteligencia artificial.
El proyecto comienza con la premisa que en la actualidad existen muchos usuarios de smartwatches que usan aplicaciones de entrenamiento
que generan unas cantidades masivas de datos. Estos datos no etiquetados pueden servir entre muichas otras cosas a clasificar a los usuarios de estas aplicaciones en distintos perfiles en funcion de los datos obtenidos. Gracias a estos perfiles se podrian ofrecer a los usuarios clasificados, planes de entrenamientos mejor ajustados a sus caracteristicas fisiologicas de esta manera, se podria mejorar su rendimiento y capacidades fisiologicas de una manera mas efectiva.
Para el experimento se ha utilizado el data set de Endomondo, el cual parte de mediciones realizadas por smartwatches en mas de 65.000 sesiones de entrenamientos de runnig.
Durante el desarrollo del experimento se han utilizado tres algoritmos de aprendizaje automatico no supervisado:
- K-means
- DBSCAN
- Clustering Jerarquico
Como resultado final del experimento, tras analizar los distintos modelos, el mejor output y metricas ha sido K-means. Este con un k=5 ha conseguido hacer una division efectiva del dataset en 5 perfiles de corredor muy diferenciados entre ellos.
Con este experimento se muestra una solucion escalable y valida para la generacion de perfiles a partir de datos recogidos por smartwatches.
## Descripción del análisis

El flujo principal del notebook `main.ipynb` es el siguiente:
- Lectura del dataset original `data/endomondoHR_proper.json`.
- Selección de sesiones de tipo `run`.
- Extracción de características agregadas por sesión: distancia, duración, velocidad GPS, ritmo, frecuencia cardiaca y elevación.
- Filtrado y limpieza de datos para eliminar sesiones inválidas o atípicas.
- Agregación por corredor usando estadísticas robustas (medianas y desviaciones estándar).
- Normalización y reducción dimensional con PCA.
- Clustering con varios métodos:
  - K-Means.
  - DBSCAN.
  - Clustering jerárquico de Ward.

## Resultados clave

- El notebook actual ajusta el modelo K-Means con `k=5`.
- Se comparan las tres metodologías y se generan visualizaciones de ambos modelos.
- El resultado final del análisis se guarda en `data/run_profiles_clustered.csv` con etiquetas de cluster y nombres de perfil.

## Archivos generados

Al ejecutar el notebook se generan archivos de datos y gráficas como:
- `data/run_features.csv`
- `data/run_clean.csv`
- `data/run_profiles_raw.csv`
- `data/run_profiles_clustered.csv`
- `data/cluster_resumen.csv`
- `data/cluster_zscore.csv`
- `fig_clusters_pca.png`
- `fig_clusters_heatmap.png`
- `fig_kmeans_tamanos.png`
- `fig_dbscan_kdist.png`
- `fig_dbscan_modelo.png`
- `fig_ward_dendrograma.png`
- `fig_ward_pca.png`
- `fig_ward_heatmap.png`
- `fig_ward_tamanos.png`
- `fig_comparativa_metricas.png`
- `fig_scatter_3modelos.png`
- `fig_distribucion_3modelos.png`
- `fig_perfiles_huella.png`

## Dependencias

Para ejecutar el notebook necesitas al menos:
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy

## Uso

1. Coloca el dataset `endomondoHR_proper.json` en la carpeta `data/`.
2. Abre `main.ipynb` en Jupyter Notebook o JupyterLab.
3. Ejecuta las celdas en orden.

## Fuente de datos

El dataset utilizado se puede descargar desde:
https://cseweb.ucsd.edu/~jmcauley/datasets.html#endomondo

## Nota

Este repositorio es una versión de trabajo del proyecto y puede necesitar el dataset original y dependencias específicas para ejecutarse correctamente.