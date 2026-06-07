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

### 02 - AmericasBarometer Costa Rica 2023 — Citizen Profiles & Democratic Attitudes
**Dataset:** AmericasBarometer Costa Rica 2023 (LAPOP, N=1,527)  
**Tools:** Python, pandas, scikit-learn, matplotlib, seaborn  
**Topics:** EDA, PCA, K-means clustering, logistic regression, political behavior

**Key findings:**
- Four citizen profiles identified via PCA + K-means: Escépticos autoritarios (14.4%),
  Demócratas liberales (28.3%), Demócratas iliberales (36.9%), Liberales semidemócratas (20.4%).
- Logistic regression models achieved Pseudo R² = 0.142, identifying key predictors
  of support for democratic norms.
- Results replicate and extend official LAPOP 2023 findings for Costa Rica.

| Notebook | Description |
|----------|-------------|
| 📓 [01_EDA.ipynb](./AmericasBarometer%202023/01_EDA.ipynb) | Exploratory analysis replicating official LAPOP 2023 findings |
| 📓 [02_ACP_clustering.ipynb](./AmericasBarometer%202023/02_ACP_clustering.ipynb) | PCA + K-means: four citizen profiles |
| 📓 [03_regresion_logistica.ipynb](./AmericasBarometer%202023/03_regresion_logistica.ipynb) | Logistic regression, two models |

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
