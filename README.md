# Data Analysis Portfolio
A collection of data analysis projects covering the full analytical workflow — 
from exploratory analysis and data cleaning to visualization and insight generation —
using Python and industry-standard libraries.

---

## Projects

### 01 - Smartphone Usage and Addiction Analysis
**Dataset:** 7,500 records of smartphone usage behavior  
**Tools:** Python, pandas, matplotlib, seaborn  
**Topics:** EDA, data cleaning, univariate analysis, bivariate analysis, 
correlation analysis, outlier detection

**Key findings:**
- Screen time variables (`daily_screen_time_hours`, `social_media_hours`) are the 
  strongest predictors of addiction.
- Demographic variables (age, gender) and behavioral indicators (sleep, stress) 
  show no meaningful relationship with addiction.
- Dataset shows strong indicators of being synthetically generated.

📓 [View Notebook](./Data_Analyst.ipynb)

---

### 02 - Barómetro de las Américas Costa Rica 2023 — Perfiles Ciudadanos y Actitudes Democráticas
**Dataset:** Barómetro de las Américas Costa Rica 2023 (LAPOP, N=1,527)  
**Herramientas:** Python, pandas, scikit-learn, matplotlib, seaborn  
**Temas:** EDA, ACP, clustering K-means, regresión logística, comportamiento político

**Hallazgos principales:**
- Se identificaron cuatro perfiles ciudadanos mediante ACP + K-means: Escépticos autoritarios (14.4%),
  Demócratas liberales (28.3%), Demócratas iliberales (36.9%), Liberales semidemócratas (20.4%).
- Los modelos de regresión logística alcanzaron un Pseudo R² = 0.142, identificando predictores
  clave del apoyo a las normas democráticas.
- Los resultados replican y amplían los hallazgos oficiales de LAPOP 2023 para Costa Rica.

| Cuaderno | Descripción |
|----------|-------------|
| 📓 [01_EDA.ipynb](./AmericasBarometer2023/01_EDA.ipynb) | Análisis exploratorio replicando hallazgos oficiales LAPOP 2023 |
| 📓 [02_ACP_clustering.ipynb](./AmericasBarometer2023/02_ACP_clustering.ipynb) | ACP + K-means: cuatro perfiles ciudadanos |
| 📓 [03_regresion_logistica.ipynb](./AmericasBarometer2023/03_regresion_logistica.ipynb) | Regresión logística, dos modelos |

---

## Tools & Libraries
- Python 3.13
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

## Author
Steven Herrera Bonilla  
[GitHub](https://github.com/herrerasteven01-ops)
