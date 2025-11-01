📘 README — Segmentación con K-Means
📋 Descripción general

Este proyecto realiza un análisis exploratorio y segmentación de clientes utilizando el algoritmo K-Means Clustering, con el propósito de identificar patrones de comportamiento y perfiles diferenciados en función de variables demográficas y de gasto.

Se aplican tres modelos de clustering con diferentes combinaciones de variables para comparar resultados y evaluar cuál genera una segmentación más coherente y útil para la toma de decisiones.

🎯 Objetivos

Analizar y preparar los datos para un correcto modelado con K-Means.

Evaluar distintas combinaciones de variables para determinar los factores más relevantes en la segmentación.

Identificar grupos de clientes con características y comportamientos diferenciados.

Comparar el rendimiento de los modelos mediante la métrica Silhouette Score.

Generar insights que apoyen estrategias de marketing, fidelización o personalización de servicios.

⚙️ Metodología
1️⃣ Exploración inicial del dataset

Revisión de la estructura, tipos de datos y valores nulos.

Análisis descriptivo de variables numéricas: distribución, valores atípicos y correlaciones.

Visualizaciones iniciales con histogramas y gráficos de dispersión.

2️⃣ Preparación de los datos

Estandarización de las variables con StandardScaler para asegurar igualdad de escala.

Selección del número de clusters óptimo mediante el método del codo (Elbow Method).

3️⃣ Aplicación del algoritmo K-Means

Se entrenan tres modelos distintos para observar cómo cambia la estructura de los clusters según las variables utilizadas.

🔍 Modelos de Clustering
🧩 Modelo 1: Segmentación por Ingresos y Puntuación de Gastos

Variables utilizadas: Annual Income (k$) y Spending Score (1-100)

Número de clusters óptimo: 3

Silhouette Score: 0.44
📊 Este modelo permite identificar tres grupos principales de clientes según su nivel de ingresos y hábitos de gasto. Es una segmentación clásica que muestra la relación entre poder adquisitivo y comportamiento de compra.

👥 Modelo 2: Segmentación por Edad y Puntuación de Gastos

Variables utilizadas: Age y Spending Score (1-100)

Número de clusters óptimo: 5

Silhouette Score: 0.56
📈 En este modelo se observan patrones más definidos: los clientes más jóvenes tienden a tener una mayor puntuación de gasto, mientras que los de mayor edad presentan un comportamiento más moderado. Este modelo logra la mejor separación de grupos según el Silhouette Score.

💼 Modelo 3: Segmentación por Edad, Ingresos y Puntuación de Gastos

Variables utilizadas: Age, Annual Income (k$) y Spending Score (1-100)

Número de clusters óptimo: 4

Silhouette Score: 0.39
📉 Aunque incluye más variables, los clusters se solapan ligeramente. Aun así, este modelo ofrece una visión tridimensional del comportamiento del cliente, integrando variables demográficas y económicas.

📊 Resultados e Insights

El Modelo 2 (Edad + Spending Score) presenta la mejor cohesión y separación de grupos. Este modelo, con un Silhouette Score de 0.56 y 5 clusters, es el más robusto estadísticamente.

Los clusters permiten identificar perfiles distintos: jóvenes con alto gasto, adultos de gasto medio y mayores con menor frecuencia de consumo.

La combinación de edad y comportamiento de compra es el factor más determinante en la segmentación. Son las dos variables más influyentes y con la relación más limpia y diferenciadora en este conjunto de datos.

El análisis ofrece información clave para acciones de marketing segmentado, estrategias de precios o optimización de experiencias personalizadas. Dado el éxito del Modelo 2, la estrategia de marketing debe pivotar hacia el ciclo de vida y las tendencias generacionales.

🧰 Tecnologías utilizadas

Python 3

Pandas / NumPy

Matplotlib / Seaborn

Scikit-learn

🧠 Conclusiones

Este ejercicio demuestra cómo la elección de variables impacta directamente en la estructura de los clusters.
La comparación entre modelos permite seleccionar el enfoque más coherente para describir los diferentes tipos de clientes y respaldar decisiones estr
