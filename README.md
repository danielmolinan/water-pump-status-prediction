# Water Pump Status Prediction
Multiclass classification model to predict the operational status of water pumps in Tanzania, distinguishing between **functional**, **non-functional**, and **functional but in need of repair** pumps. Project developed as part of the Master's in Data Science, Big Data & Business Analytics at Universidad Complutense de Madrid.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sjtWvhHV0WKTMvJcbaHPlwcft9Wn1ORL?usp=sharing)

---

## Results

| Model | Accuracy |
|--------|----------|
| Baseline (majority class) | 0.543 |
| Random Forest (no tuning) | 0.791 |
| **Random Forest (optimized)** | **0.813** |
| XGBoost | 0.809 |

---

## Problem description
The dataset comes from DrivenData's **Pump it Up** competition, based on real data from Tanzania's Ministry of Water. It contains information on ~59,000 water pumps distributed across the country, including geographic, technical, and management features.

The goal is to predict each pump's status into one of three categories:

- `functional` — The pump is working correctly
- `non functional` — The pump is not working
- `functional needs repair` — The pump works but requires repair

Correctly identifying pumps in poor condition allows interventions to be prioritized and helps guarantee access to safe drinking water for affected communities.

---

## Methodology

### 1. Exploratory Data Analysis (EDA)
- Inspection of missing values and class distribution
- Analysis of geographic, categorical, and numerical variables
- Identification of redundant or low-variance columns

### 2. Preprocessing
- Imputation of missing values
- Encoding of categorical variables with `LabelEncoder`
- Scaling of numerical variables
- Reproducible transformation pipeline with Scikit-learn

### 3. Modeling
- Baseline: majority-class prediction
- Random Forest: training with manual hyperparameter tuning (`n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`)
- XGBoost: training and comparison of results
- Evaluation using accuracy and confusion matrix

---

## Technologies
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat&logo=googlecolab&logoColor=white)

- **Modeling:** Scikit-learn · XGBoost
- **Analysis and transformation:** Pandas · NumPy
- **Visualization:** Matplotlib · Seaborn
- **Environment:** Google Colab

---

## Repository structure
```
water-pump-status-prediction/
│
├── README.md
├── notebook.ipynb        # Full notebook with code and results
└── requirements.txt      # Project dependencies
```

---

## How to run
1. Open the notebook in Google Colab using the button above
2. Run the cells in order
3. The dataset must be available in your Google Drive; it can be downloaded from the link included in the notebook

---

## References
- Dataset: [Pump it Up — DrivenData](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/)

---

## Author
**Daniel Molina Novoa** · Data Analyst
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-molina-novoa/)
[![GitHub](https://img.shields.io/badge/GitHub-danielmolinan-181717?style=flat&logo=github&logoColor=white)](https://github.com/danielmolinan)
