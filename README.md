# Data Experience — Análisis de Google Play Store Apps

Proyecto final **Data Experience**. Analizamos un dataset real de Google Play Store para aplicar lo aprendido en los módulos de DATA EXPERIENCE: selección, exploración, limpieza, análisis estadístico, visualización...

## Dataset

**Google Play Store Apps** (Kaggle) — 10,841 apps con columnas como categoría, calificación, número de reseñas, instalaciones, tamaño, precio y versión de Android soportada.

**Justificación:** como estudiantes de Ingeniería de Sistemas, escogimos este dataset porque conecta directamente con el ciclo de vida del software, en este caso de las apps: calidad de datos en catálogos de apps, modelos de monetización, compatibilidad de versiones (de android) y comportamiento real de usuarios.

## Estructura del proyecto

El trabajo está desarrollado en un único notebook: [`proyecto_data_experience.ipynb`](proyecto_data_experience.ipynb), dividido en tres fases:

### Fase 1 — Selección, exploración y preparación de datos
- Carga y exploración inicial del dataset (tipos de variable, nulos, duplicados).
- Detección de problemas reales: una fila corrupta con columnas corridas, 483 duplicados exactos, columnas numéricas guardadas como texto (`Installs`, `Price`, `Size`).
- Limpieza y transformación de los datos hacia un dataset depurado (`googleplaystore_clean.csv`).


### Fase 2 — Análisis estadístico
- Medidas de tendencia central y dispersión (media, mediana, moda, varianza, desviación estándar).
- Comparación entre variables (apps gratis vs. pagas, rating por categoría).
- Detección de outliers (método IQR) y estrategias de manejo: conservación, transformación logarítmica, estandarización z-score y capping en donde explicamos cuál se usó para cada caso y por qué.
- Validación cruzada entre columnas para diferenciar errores reales de outliers genuinos (ej. apps con más reseñas que instalaciones).

### Fase 3 — Visualización, storytelling y modelo predictivo
- Visualizaciones finales (dispersión, barras, histogramas) que resumen los hallazgos.
- Narrativa de datos conectando las tres fases del proyecto.
- Modelo de regresión lineal para predecir el `Rating` de una app a partir de reseñas, instalaciones, tamaño y precio — con evaluación honesta de su desempeño (R², MAE, RMSE).
- Propuesta de aplicación profesional del análisis en un entorno de desarrollo/producto de software.

## Cómo ejecutar el proyecto

1. Clona este repositorio.
2. Abre `proyecto_data_experience.ipynb` en Jupyter Notebook o en [Google Colab](https://colab.research.google.com/).
3. Asegúrate de que `googleplaystore.csv` esté en la misma carpeta que el notebook.
4. Instala las dependencias si hace falta:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
5. Ejecuta todas las celdas en orden.

## Tecnologías utilizadas

- Python
- pandas, numpy — manejo y limpieza de datos
- matplotlib, seaborn — visualización
- scikit-learn — modelo de regresión lineal

## Autoría

Elen Zawady,
Daniela Salcedo,
Maicol Gomez.
