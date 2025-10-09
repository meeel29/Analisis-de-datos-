# 🚢 Análisis de Datos – Titanic Dataset

Este proyecto corresponde al taller de **Análisis de Datos** (Semana 4, Prof. Daniel Alexis Nieto Mora).  
El propósito es aplicar técnicas de **Análisis Exploratorio de Datos (EDA)** usando el dataset del Titanic.  
En este trabajo revisamos valores faltantes y atípicos, analizamos la distribución de los datos y exploramos las relaciones entre variables con diferentes visualizaciones.

---

## 📂 Estructura del repositorio

```
├── train.csv                      # Dataset base (Titanic - Kaggle)
├── Valores_Faltantes.ipynb        # Análisis de valores faltantes
├── Valores_Atípicos.ipynb         # Identificación de outliers
├── Distribuciones.ipynb           # Análisis de distribuciones
├── Analisis_Univariado.ipynb      # Análisis univariado
├── Analisis_Multivariado.ipynb    # Análisis multivariado
├── Relaciones_Entre_Variables.ipynb # Relaciones entre variables
├── analisis_de_datos.ipynb        # Analisis de datasets
├── PCA_2D.ipynb                   # Proyección dataset en 2D despues de aplicar PCA
├── X_procesado_escalado.ipynb     # Variables predictorias normalizadas
├── y_target.ipynb                 # Variable objetivo separada del resto de columnas
├── AnalisisTitanicParte3.ipynb    # Analisis preprocesamiento y PCA
```

---

## 🎯 Objetivos del taller
 
1. **Análisis de distribuciones**  
   - Explorar la forma de las variables numéricas con histogramas y gráficas de densidad.  
   - Revisar sesgos y curtosis.  
   - Mencionar posibles transformaciones (como logaritmo o estandarización).  

2. **Análisis univariado**  
   - Estadísticos descriptivos de cada variable.  
   - Histogramas con curvas de densidad.  
   - Boxplots para ver outliers.  
   - Gráficas de barras para variables categóricas.  

3. **Análisis multivariado**  
   - Matriz de correlación y mapa de calor.  
   - Diagramas de dispersión (ej. `Age` vs `Fare` con `Survived`).  
   - Tablas cruzadas (ej. `Sex` vs `Survived`, `Pclass` vs `Survived`).  
   - Heatmap de tasas de supervivencia combinando `Pclass` y `Sex`.  

4. **Relaciones entre variables**  
   - Pairplot para ver relaciones entre numéricas.

---

## 🛠️ Tecnologías utilizadas

- **Python 3.x**
- **pandas** → manipulación de datos  
- **numpy** → operaciones matemáticas  
- **matplotlib / seaborn** → visualizaciones  
- **scipy.stats** → skewness y kurtosis  

---

## 📊 Principales hallazgos

- **Valores faltantes**:  
  - `Age` con ≈20% de datos faltantes.  
  - `Cabin` con más del 70% faltante → no es útil para el análisis.  
  - `Embarked` con solo 2 valores faltantes.  

- **Valores atípicos**:  
  - `Fare` tiene outliers importantes (>500).  
  - `Age` muestra extremos (bebés y ancianos).  
  - `SibSp` y `Parch` reflejan familias grandes poco comunes.  
  
- **Distribuciones**: variables como `Fare`, `SibSp` y `Parch` muestran mucho sesgo a la derecha y presencia de valores extremos.  
- **Univariado**: `Age` es casi normal, mientras que `Fare` evidencia la gran desigualdad económica entre pasajeros.  
- **Multivariado**: `Sex` y `Pclass` son claves para explicar la supervivencia.  
- **Relaciones**: el pairplot confirma que los pasajeros de tarifas más altas y mejor clase tenían más chances de sobrevivir.  
- **Visualizaciones**: los gráficos ayudan a entender la diferencia social y de género en el desenlace del Titanic.  

---

## 👥 Integrantes del equipo

- Sara Estefania Bermudez Alvarez 
- Melissa Mahecha Garcia 
- Camilo Vásquez Suarez
 
---

## 🎥 Video explicativo

👉 [Video](https://drive.google.com/file/d/1Gg-ZAOuYzXjd0AOAAFnOP9r16TuQ9g5C/view?usp=sharing)

---

## 📑 Documento complementario

Además de los notebooks incluidos en este repositorio, se preparó un documento en Google Drive con un análisis más detallado y reflexiones adicionales.  

👉 [Documento complementario del análisis](https://docs.google.com/document/d/15bqnDajFsUy4NNlnukhAW_Sq9oHov9HGIvuNbO58cJI/edit?usp=sharing)
