# Predicción del Estado de Bombas de Agua

Modelo de clasificación multiclase para predecir el estado operativo de bombas de agua en Tanzania, distinguiendo entre bombas **funcionales**, **no funcionales** y **funcionales pero que necesitan reparación**. Proyecto desarrollado como parte del Máster en Data Science, Big Data & Business Analytics en la Universidad Complutense de Madrid.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sjtWvhHV0WKTMvJcbaHPlwcft9Wn1ORL?usp=sharing)

---

## Resultados

| Modelo | Accuracy |
|--------|----------|
| Baseline (clase mayoritaria) | 0.543 |
| Random Forest (sin tuning) | 0.791 |
| **Random Forest (optimizado)** | **0.813** |
| XGBoost | 0.809 |

---

## Descripción del problema

El dataset proviene de la competición **Pump it Up** de DrivenData, basada en datos reales del Ministerio de Agua de Tanzania. Contiene información sobre ~59.000 bombas de agua distribuidas por el país, incluyendo características geográficas, técnicas y de gestión.

El objetivo es predecir el estado de cada bomba en una de tres categorías:

- `functional` — La bomba funciona correctamente
- `non functional` — La bomba no funciona
- `functional needs repair` — La bomba funciona pero requiere reparación

Identificar correctamente las bombas en mal estado permite priorizar intervenciones y garantizar el acceso al agua potable a las comunidades afectadas.

---

## Metodología

### 1. Análisis exploratorio (EDA)
- Inspección de valores nulos y distribución de clases
- Análisis de variables geográficas, categóricas y numéricas
- Identificación de columnas redundantes o con baja varianza

### 2. Preprocesamiento
- Imputación de valores nulos
- Codificación de variables categóricas con `LabelEncoder`
- Escalado de variables numéricas
- Pipeline de transformación reproducible con Scikit-learn

### 3. Modelado
- Baseline: predicción por clase mayoritaria
- Random Forest: entrenamiento con ajuste manual de hiperparámetros (`n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`)
- XGBoost: entrenamiento y comparación de resultados
- Evaluación con accuracy y matriz de confusión

---

## Tecnologías

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat&logo=googlecolab&logoColor=white)

- **Modelado:** Scikit-learn · XGBoost
- **Análisis y transformación:** Pandas · NumPy
- **Visualización:** Matplotlib · Seaborn
- **Entorno:** Google Colab

---

## Estructura del repositorio

```
water-pump-status-prediction/
│
├── README.md
├── notebook.ipynb        # Notebook completo con código y resultados
└── requirements.txt      # Dependencias del proyecto
```

---

## Cómo ejecutar

1. Abre el notebook en Google Colab con el botón de arriba
2. Ejecuta las celdas en orden
3. El dataset debe estar disponible en tu Google Drive; se puede descargar desde el enlace incluido en el notebook

---

## Referencias

- Dataset: [Pump it Up — DrivenData](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/)

---

## Autor

**Daniel Molina Novoa** · Data Analyst  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-molina-novoa-78106925a/)
[![GitHub](https://img.shields.io/badge/GitHub-danielmolinan-181717?style=flat&logo=github&logoColor=white)](https://github.com/danielmolinan)
