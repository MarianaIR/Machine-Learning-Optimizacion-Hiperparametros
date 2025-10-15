# ⚙️ MACHINE LEARNING: OPTIMIZACIÓN DE HIPERPARÁMETROS

[![Python](https://img.shields.io/badge/Python-3670A0?style=flat&logo=python&logoColor=ffdd54)](https://www.python.org/)  
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)

Este proyecto aborda una etapa avanzada y crítica en Machine Learning: la **Optimización de Hiperparámetros**. Se enfoca en mejorar el rendimiento y la capacidad de generalización de un modelo predictivo, como un **Árbol de Decisión**, al encontrar la mejor combinación de sus parámetros internos (hiperparámetros).

---

## 🧠 Contenido del Proyecto

### 1️⃣ El Problema de la Optimización
- **Hiperparámetros vs. Parámetros:** Los **parámetros** son aprendidos por el modelo a partir de los datos (ej. pesos en una regresión), mientras que los **hiperparámetros** son definidos *antes* del entrenamiento (ej. la profundidad máxima de un árbol).
- **Impacto:** Una mala elección de hiperparámetros puede llevar al **sobreajuste (*overfitting*)** o al **subajuste (*underfitting*)**, resultando en un modelo inútil.

### 2️⃣ Dataset y Modelo de Referencia
- **Dataset:** Se utiliza un dataset de vehículos que incluye el **precio**, el estado de **venta** (`vendido: 1/0`), la **edad del modelo** y los **kilómetros por año**.
- **Modelo Inicial:** Se establece un modelo de clasificación inicial (probablemente un **Árbol de Decisión**) con hiperparámetros por defecto para medir su rendimiento base antes de la optimización.

### 3️⃣ Métodos de Optimización de Hiperparámetros
El proyecto implementa y compara dos estrategias principales para la búsqueda del mejor conjunto de hiperparámetros:

#### A. Búsqueda por Grilla (Grid Search)
- **Concepto:** Consiste en definir una **grilla exhaustiva** (un diccionario de todas las combinaciones posibles de hiperparámetros) y entrenar el modelo con *cada* combinación.
- **Herramienta:** Se utiliza `GridSearchCV` de Scikit-learn, combinándolo con la **Validación Cruzada** (`K-Fold`) para evaluar de forma robusta cada combinación y elegir la mejor.
- **Resultado:** Garantiza encontrar el mejor conjunto dentro de la grilla definida.

#### B. Búsqueda Aleatoria (Random Search)
- **Concepto:** En lugar de probar todas las combinaciones, `Random Search` prueba un **subconjunto aleatorio** de combinaciones dentro de un rango definido.
- **Ventaja:** Es mucho más **rápida** y eficiente en términos de recursos computacionales que `Grid Search`, especialmente cuando el número de hiperparámetros es grande.

### 4️⃣ Optimización del Árbol de Decisión
Se optimizan hiperparámetros clave del Árbol de Decisión, como:
- `max_depth` (Profundidad máxima del árbol)
- `min_samples_leaf` (Número mínimo de muestras en un nodo hoja)
- `criterion` (Función para medir la calidad de una división, ej. Gini o Entropía).

---

## 🛠️ Librerías Utilizadas

| Librería | Uso principal |
|:---:|:---:|
| **Scikit-learn** | Implementación de modelos (`DecisionTree`), `GridSearchCV`, `RandomizedSearchCV` y métricas|
| **Pandas** | Carga y manipulación de los datos del mercado de vehículos |

---

## 🎯 Objetivo del Proyecto
El objetivo es dominar las técnicas de **optimización automática** para refinar y mejorar modelos de Machine Learning. El proyecto enseña cuándo y cómo utilizar **Grid Search** y **Random Search** para maximizar el rendimiento de un modelo, garantizando que el modelo final no solo sea preciso sino que también generalice bien a datos no vistos.

---

## 📈 Resultados Clave
- Se demuestra la **mejora en el rendimiento** (ej. mayor `Accuracy` o `F1-Score`) después de aplicar la optimización de hiperparámetros en comparación con el modelo base.
- Se identifica y aplica el **mejor conjunto de hiperparámetros** encontrado, lo que minimiza el riesgo de sobreajuste.
- Se proporciona una comprensión práctica de la **compensación entre la exhaustividad (Grid Search) y la eficiencia (Random Search)** en la optimización de modelos.

