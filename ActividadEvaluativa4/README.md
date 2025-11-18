## 📘 Análisis de Datos – Modelos de Machine Learning

Subimos los notebooks desarrollados para el análisis, preprocesamiento y experimentación con distintos modelos de Machine Learning supervisado y no supervisado, aplicados a dos tipos de problemas:

- Predicción del rendimiento académico de estudiantes.
- Clasificación de sentimiento en texto (reseñas).

Además incluimos técnicas de reducción de dimensionalidad, vectorización de texto, visualizaciones, métricas, y la comparación detallada de tres métodos de ML.

---

## 📂 Contenido de los notebooks

---

### 1. Predicción del rendimiento académico – Student Performance (Math)

#### ✔ Descripción del problema
Se busca predecir la variable **GradeClass** (alto / medio / bajo) derivada de la nota final G3, usando características académicas, personales y contextuales de estudiantes.

#### ✔ Preprocesamiento realizado
- Imputación de valores faltantes (mediana/moda).
- Codificación One-Hot para variables categóricas.
- Estandarización de variables numéricas.
- División **train/test 75/25**, estratificada.

#### ✔ Modelos evaluados
- Regresión Logística  
- Árboles de Decisión  
- Random Forest  

#### ✔ Visualizaciones
- Histogramas y distribución de notas.
- Matriz de correlación.
- Importancia de características según los modelos.

---

### 2. Clasificación de Sentimiento en Texto  
*(Basado en reseñas positivas/negativas)*

#### ✔ Procesamiento de texto
- Limpieza: minúsculas, eliminación de puntuación, stopwords y tokens ruidosos.
- Tokenización y vectorización usando **TF-IDF** (máx. features = 5000).
- Se usaron **unigramas**.
- Los **bigramas NO se usaron** por costo computacional y dispersión.

#### ✔ Modelos comparados
- Naive Bayes  
- Regresión Logística  
- SVM (LinearSVC)

#### ✔ Resultados principales
- **SVM** tuvo la mejor precisión y generalización.
- Regresión Logística también funcionó muy bien en texto de alta dimensionalidad.
- Naive Bayes fue el más rápido, pero con menor rendimiento.

#### ✔ Nubes de palabras
Se generaron wordclouds para reseñas positivas y negativas.  
Se encontró que algunas palabras aparecen en ambos grupos debido a:
- Reseñas mixtas
- Palabras neutrales (producto, libro…)
- Ruido del dataset
- Eliminación del contexto en la limpieza

#### ✔ Extracción de palabras más importantes
Se listaron las **top 20** palabras positivas y negativas según los coeficientes de Regresión Logística.

---

### 3. Reducción de Dimensionalidad

#### ✔ PCA (Componentes Principales)
- Reduce miles de dimensiones a 2.
- Se observó mezcla entre clases (normal en texto vectorizado).

#### ✔ t-SNE
- Captura relaciones no lineales.
- Formó grupos mejor separados que PCA.

#### ✔ Wordclouds + Distribuciones
- Ayudaron a interpretar patrones en ambos tipos de reseñas.

---

## 📊 Métricas utilizadas
- Accuracy  
- F1-Score  
- Precision / Recall  
- Matriz de confusión  
- (Para clustering) Silhouette score

---

## 📝 Conclusiones
- La calidad del **preprocesamiento** afecta directamente el desempeño de los modelos.
- Los modelos lineales (SVM, Regresión Logística) funcionan muy bien con TF-IDF.
- En Student Performance, **G1 y G2** son altamente predictivas de G3.
- PCA muestra mezcla entre clases; **t-SNE** ofrece mejor separación visual.
- El proyecto demuestra un flujo completo:  
  **EDA → Limpieza → Vectorización → Modelado → Métricas → Reducción → Interpretación.**

---

## 👥 Integrantes
- Sara Estefania Bermúdez Álvarez  
- Melissa Mahecha García  
- Camilo Vásquez Suárez  

---

## 🎬 Video
El video correspondiente a los ejercicios se encuentra en:  
https://youtu.be/OMHdATuk4zQ
