# Perfiles de Ciudadanía Política en Costa Rica 2023
### Un análisis del AmericasBarometer con machine learning

**Autor:** Stiven Herrera Bonilla  
  
**Fecha:** 2026

---

## Descripción

Este proyecto analiza las actitudes democráticas de 1,527 costarricenses
usando datos del AmericasBarometer LAPOP 2023 (Vanderbilt University).
El objetivo es identificar perfiles de ciudadanía política mediante
técnicas de machine learning no supervisado y modelar los predictores
de satisfacción democrática.

El análisis replica y extiende los hallazgos del informe oficial
*Pulso de la Democracia en Costa Rica 2023* (Alfaro, 2024).

---

## Estructura del proyecto

├── notebooks/
│   ├── 01_EDA.ipynb                  # Análisis exploratorio de datos
│   ├── 02_ACP_clustering.ipynb       # ACP + K-means
│   └── 03_regresion_logistica.ipynb  # Regresión logística binaria
├── outputs/
│   ├── 01_satisfaccion_democracia.png
│   ├── 02_preferencia_democracia.png
│   ├── 03_apoyo_sistema_distribuciones.png
│   ├── 04_heatmap_confianza.png
│   ├── 05_perfil_sociodemografico.png
│   ├── 06_satisfaccion_por_grupo.png
│   ├── 07_migracion_por_grupo.png
│   ├── 08_scree_plot.png
│   ├── 09_cargas_pca.png
│   ├── 10_metodo_codo.png
│   ├── 11_clusters_pca.png
│   ├── 12_radar_clusters.png
│   ├── 13_comparacion_perfiles.png
│   ├── 14_efectos_marginales.png
│   ├── 15_comparacion_modelos.png
│   └── 16_efectos_clusters.png
├── .gitignore
└── README.md

---

## Módulos

### Módulo 1 — Análisis Exploratorio de Datos (EDA)

- Carga y exploración del dataset (1,527 casos × 219 variables)
- Verificación de variables y corrección de nomenclatura entre rondas
- Análisis de valores faltantes
- Replicación de hallazgos del informe oficial:
  - Satisfacción con la democracia: **61.4%** (vs 61% oficial ✓)
  - Preferencia por la democracia: **72.1%** (vs 72% oficial ✓)
- Heatmap de correlaciones de confianza institucional
- Perfil sociodemográfico de la muestra
- Cruces de satisfacción democrática y actitudes migratorias por grupos

### Módulo 2 — ACP + Clustering K-means

- Estandarización de 9 variables actitudinales (B1-B6, D1-D4)
- ACP: 2 componentes principales explican el **59.3%** de la varianza
- K-means con K=4 (seleccionado por método del codo y coeficiente de silueta)
- Identificación de cuatro perfiles de ciudadanía política:

| Cluster | Nombre | N | % | Apoyo sistema | Tolerancia |
|---------|--------|---|---|---------------|------------|
| C1 | Demócratas liberales | 414 | 28.3% | Muy alto | Muy alta |
| C2 | Demócratas iliberales | 540 | 36.9% | Alto | Muy baja |
| C3 | Liberales semidemócratas | 299 | 20.4% | Moderado | Muy alta |
| C0 | Escépticos autoritarios | 211 | 14.4% | Muy bajo | Baja |

- Comparación con los perfiles Fuzzy Sets del informe oficial

### Módulo 3 — Regresión Logística Binaria

- Variable dependiente: satisfacción con la democracia (`pn4_bin`)
- Modelo 1 (replicación): Pseudo R²=0.107, N=1,386
- Modelo 2 (extendido con clusters): Pseudo R²=0.142, N=1,386
- Predictores significativos: evaluación del presidente (+8.5pp),
  corrupción (-6.3pp), seguridad (+5.8pp), interés político (+4.1pp)
- Hallazgo central: los liberales semidemócratas (C3) muestran la
  menor satisfacción democrática de todos los clusters

---

## Hallazgo central

> Más del **51%** de la ciudadanía costarricense combina apoyo
> institucional con baja tolerancia política (demócratas iliberales)
> o desconfianza en ambas dimensiones (escépticos autoritarios).
> Esto cuestiona el imaginario excepcionalista del país como democracia
> consolidada y conecta con la literatura sobre erosión democrática
> (Levitsky y Ziblatt, 2018).

---

## Tecnologías utilizadas

- Python 3.13
- pandas, numpy
- scikit-learn (PCA, KMeans, silhouette_score)
- statsmodels (regresión logística, efectos marginales)
- matplotlib, seaborn

---

## Fuente de datos

LAPOP Lab, Vanderbilt University.  
*AmericasBarometer Costa Rica 2023* (N=1,527).  
Disponible en: [www.vanderbilt.edu/lapop](https://www.vanderbilt.edu/lapop)

> **Nota:** El archivo de datos (`.dta`) no está incluido en este
> repositorio por restricciones de licencia. Puede solicitarse
> directamente a LAPOP Lab.

---

## Referencias

- Alfaro Redondo, R. (2024). *Pulso de la Democracia en Costa Rica 2023*.
  LAPOP Lab / Vanderbilt University.
- Levitsky, S. y Ziblatt, D. (2018). *How Democracies Die*. Crown Publishing.
- Pignataro, A. y Treminio, I. (2019). Reto económico, valores y religión
  en las elecciones de Costa Rica 2018. *Revista de Ciencia Política*, 39(2).
- Treminio, I. y Pignataro, A. (2021). Jóvenes y el voto por la derecha
  radical en Costa Rica. *Población & Sociedad*, 28(2).