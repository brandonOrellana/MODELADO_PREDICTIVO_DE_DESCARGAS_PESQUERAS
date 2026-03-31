# Predicción de Capturas Pesqueras en Argentina – Proyecto Final Integrador

El repositorio contiene los notebooks y los datos para el Proyecto Final Integrador del Diplomado en Ciencia de Datos y Análisis Avanzado. 
El objetivo es predecir si una descarga de flota industrial será excepcional utilizando técnicas de Machine Learning y siguiendo la metodología CRISP-DM.

## Contenido

- `CLASIFICACION DESCARGAS.ipynb`: Notebook Jupyter con el análisis de clasificación: carga de datos, EDA, ingeniería de variables, modelado (Random Forest, XGBoost, Redes Neuronales (Keras)), evaluación y comparación de resultados.
- `REGRESION DESCARGAS.ipynb`: Notebook Jupyter con el análisis de regresión: carga de datos, EDA, ingeniería de variables, modelado (Random Forest, Gradient Boosting), evaluación y comparación de resultados.
- `descarga-puerto-flota-2010-2019.csv`: Archivo descargado del portal oficial (ver instrucciones más abajo).
- `README.md`: Este archivo, que describe el proyecto, requisitos y cómo ejecutar el notebook.

## Requisitos

- Python 3.10 o superior.
- Librerías de Python: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `statsmodels`, `matplotlib`, `seaborn`, `tensorflow`, `shap`

## Instalación

1. Clona o descarga este repositorio.
2. Crea un entorno virtual:

   ```bash
   python -m venv env
   source env/bin/activate
   pip install -q pandas numpy scikit-learn xgboost statsmodels matplotlib seaborn tensorflow shap
   ```

## Descarga de Datos
1. Debes descargar los datos del portal oficial del Ministerio de Agricultura, Ganadería y Pesca de Argentina:

Accede a las fuentes oficiales:
* [Dataset 1](https://datos.magyp.gob.ar/dataset/e2f12522-4dea-495e-877a-b6d2737ae6bf/archivo/1996a5ec-7075-4062-9a79-05868fc2a2e2)
* [Dataset 2](https://datos.magyp.gob.ar/dataset/e2f12522-4dea-495e-877a-b6d2737ae6bf/archivo/77a15b4a-71e1-4b81-9732-ae0b6863c8cc)

2. Descarga y consolida los archivos en un único archivo llamado `descarga-puerto-flota-2010-2019.csv`.
3. Renombra la columna `captura` por `descarga`.

## Ejecución de los notebooks
   ```bash
   jupyter notebook REGRESION\ DESCARGAS.ipynb
   jupyter notebook CLASIFICACION\ DESCARGAS.ipynb 
   ```

### Ejecuta las celdas en orden. El notebook de CLASIFICACIÓN realiza los siguientes pasos:

 1. Comprensión del problema.
 2. Comprensión de los datos
 3. Preparación de los datos: Limpieza de datos, Feature engineering, Separación de datos
 4. Modelado: Entrenamiento de modelos
 5. Evaluación: Evaluación de métricas e interpretación
 6. Conclusiones: resultados, interpretación, valor del enfoque, limitaciones y trabajo futuro
 7. Validación temporal del modelo
 8. Bloque ROC Curve + AUC por fold (Time Series CV)
 9. Comparación final entre modelos
 10. Interpretabilidad del Modelo (Opcional - SHAP)

### Ejecuta las celdas en orden. El notebook de REGRESION realiza los siguientes pasos:

 1. Comprensión del problema.
 2. Comprensión de los Datos (EDA)
 3. Preparación de los Datos
 4. Modelado
 5. Evaluación de Modelos
 6. Conclusiones y Líneas Futuras

## Citaciones
* **Datos:** Ministerio de Agricultura, Ganadería y Pesca – Portal de Datos Abiertos de Argentina.
* **Metodología:** CRISP-DM (Cross-Industry Standard Process for Data Mining).