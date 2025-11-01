# 🛍️ Segmentación de Clientes con K-Means Clustering

## 📋 Descripción General del Proyecto

Este proyecto implementa un análisis exploratorio y de segmentación de clientes utilizando el algoritmo **K-Means Clustering**. El objetivo principal es identificar patrones de comportamiento y perfiles diferenciados en función de variables demográficas (**Edad**) y de consumo (**Ingresos** y **Gasto**).

Se aplican **tres modelos de clustering** con diferentes combinaciones de variables para comparar resultados y evaluar cuál genera la segmentación más coherente y útil para la toma de decisiones empresariales.

---

## 🎯 Objetivos Principales

* **Analizar y Preparar** los datos para un correcto modelado con K-Means.
* **Evaluar** distintas combinaciones de variables para determinar los factores más relevantes en la segmentación.
* **Identificar** grupos de clientes con características y comportamientos diferenciados (clusters).
* **Generar Insights** que apoyen estrategias de marketing, fidelización o personalización de servicios.

---

## ⚙️ Metodología Aplicada

### 1️⃣ Exploración Inicial del Dataset
* Revisión de la estructura, tipos de datos y valores nulos.
* Análisis descriptivo de variables numéricas: distribución, valores atípicos y correlaciones.
* Visualizaciones iniciales (histogramas y gráficos de dispersión).

### 2️⃣ Preparación de los Datos
* **Estandarización** de las variables con `StandardScaler` para asegurar la igualdad de escala.
* Selección del número de clusters óptimo ($k$) mediante el **Método del Codo (Elbow Method)**.

### 3️⃣ Aplicación del Algoritmo K-Means
Se entrenaron tres modelos distintos para observar cómo la estructura de los clusters cambia según las variables utilizadas:

| Modelo | Variables Utilizadas | Clusters Óptimos | **Silhouette Score** | Descripción |
| :---: | :--- | :---: | :---: | :--- |
| **Modelo 1** | **Annual Income** y **Spending Score** | 3 | **0.44** | Segmentación clásica que muestra la relación entre poder adquisitivo y el comportamiento de compra. |
| **Modelo 2** | **Age** y **Spending Score** | 5 | **0.56** | **¡El más robusto!** Muestra patrones definidos: jóvenes con mayor gasto y mayores con gasto moderado. |
| **Modelo 3** | **Age, Income** y **Spending Score** | 4 | **0.39** | Clusters con ligero solapamiento. Ofrece una visión tridimensional que es menos coherente. |

---

## 📊 Resultados e Insights Clave

* **Líder en Calidad (Modelo 2):** El Modelo 2 (Edad + Spending Score) presenta la **mejor cohesión y separación de grupos**, siendo el **más robusto estadísticamente** (Silhouette Score: **0.56**).
* **Factor Determinante:** La combinación de **Edad y Puntuación de Gasto** es el factor más influyente en la segmentación de este *dataset*.
* **Perfiles Identificados:**
    * **Adultos** con **ingresos bajos y gasto bajo**.
    * **Adultos** con **ingresos medios y gasto moderado**.
    * **Jóvenes** con **ingresos altos y gasto alto**.
    * **Jóvenes** con **ingresos bajos y gasto alto**.
* **Recomendación Estratégica:** Dado el éxito del Modelo 2, la estrategia de marketing debe pivotar hacia el **ciclo de vida y las tendencias generacionales** para optimizar la personalización y la oferta de servicios.

---

## 🧰 Tecnologías Utilizadas

* **Python 3**
* **Pandas / NumPy** (Manipulación de datos)
* **Matplotlib / Seaborn** (Visualización)
* **Scikit-learn** (Implementación de K-Means)

---

## 🧠 Conclusiones del Proyecto

Este ejercicio demuestra que la **elección de variables impacta directamente en la estructura de los clusters**. La comparación entre modelos nos permitió seleccionar el enfoque más **coherente y accionable** (Modelo 2) para describir los diferentes tipos de clientes y respaldar decisiones estratégicas basadas en datos de alto valor predictivo.
