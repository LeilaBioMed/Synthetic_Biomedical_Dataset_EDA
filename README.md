# Biomedical Data Exploration (EDA)

Exploratory Data Analysis (EDA) of synthetic biomedical indicators — **HbA1c** and **Systolic Blood Pressure (BP)** — to uncover relationships between glucose control and cardiovascular health.

---

## Project Overview

This project demonstrates **data processing, cleaning, and visualization** techniques using a **synthetic biomedical dataset** of 200 patients.  
The goal is to explore potential associations between **HbA1c** (glycated hemoglobin) and **BP_systolic** (systolic blood pressure), two key indicators of metabolic and cardiovascular health.

---

## Objectives

- Perform **descriptive statistical analysis** on HbA1c and BP.  
- Visualize data distributions and bivariate relationships.  
- Categorize patients into **clinically meaningful groups**.  
- Generate **insights and visual summaries** for biomedical interpretation.

---

## Dataset Information

| Feature | Description | Units | Typical Range |
|----------|--------------|--------|----------------|
| **PatientID** | Unique patient identifier | — | 1–200 |
| **HbA1c** | Glycated hemoglobin (indicator of long-term glucose control) | % | 4.5 – 9.5 |
| **BP_systolic** | Systolic blood pressure (upper reading) | mmHg | 90 – 180 |

**Synthetic** data was generated with mild positive correlation between HbA1c and BP_systolic to mimic realistic biomedical variability.

---

## Technologies Used

- **Python 3.x**
- **Jupyter Notebook**
- **Libraries:**
  - `pandas` — Data manipulation  
  - `numpy` — Numerical computation  
  - `matplotlib` & `seaborn` — Data visualization 

---

## Exploratory Data Analysis

### 1) Descriptive Statistics
| Metric | HbA1c | BP_systolic |
|--------:|:-------:|:-------------:|
| **Mean** | ~6.0 | ~121 |
| **Std Dev** | ~0.7 | ~16 |
| **Min–Max** | 4.5 – 8.2 | 67 – 180 |
| **Correlation (r)** | **≈ 0.32** | Positive correlation |

### 2) Distribution Insights
- **HbA1c:** Slight right-skewed; ~22% diabetic (>6.5%).  
- **BP_systolic:** Centered ~125 mmHg, mild right-skewed.  
- Moderate correlation observed (r ≈ 0.32).  

### 3) Biomedical Categorization

| Feature | Category | Thresholds |
|----------|-----------|-------------|
| **HbA1c** | Normal / Prediabetes / Diabetes | <5.7 / 5.7–6.4 / ≥6.5 |
| **BP_systolic** | Normal / Elevated / Hypertension 1–2 | <120 / 120–129 / ≥130 |

### 4) Category Counts
| Category | HbA1c (%) | BP_systolic (%) |
|-----------|:----------:|:----------------:|
| Normal | ~36% | ~47% |
| Prediabetes / Elevated | ~42% | ~25% |
| Diabetes / Hypertension | ~22% | ~28% |

### 5) Cross-Tabulation

- **Co-occurrence of Diabetes and Hypertension:**
About **33 % of diabetic patients** present with **Stage 1–2 Hypertension**, indicating a notable overlap between hyperglycemia and elevated blood pressure risk.

- **Healthy Subgroup:**
Over **60 % of normoglycemic (normal HbA1c) individuals** maintain **normal blood pressure**, reinforcing the expected association between healthy glucose regulation and vascular health.

- **Intermediate Risk Group:**
The **prediabetes group** shows a gradual rise in BP abnormalities, with **~35** % already in hypertensive stages — a potential early warning subgroup for lifestyle or medical intervention.
---

## Visualizations
Key plots generated:
- Histograms and KDE plots for distributions  
- Boxplots to visualize outliers  
- Scatterplot (HbA1c vs BP_systolic)  
- Countplots for categorical comparisons  
- Cross-tab heatmap for group overlap  

*(All visualizations produced with Seaborn & Matplotlib.)*

---

## Key Insights

- Positive correlation (r ≈ 0.3) between **HbA1c** and **BP_systolic**.  
- Prediabetes and elevated BP co-occur frequently, suggesting early metabolic risk.  
- Synthetic data behaves similarly to population studies linking **poor glycemic control** with **hypertension**.

---

## Next Steps
- Add additional biomarkers (e.g., **BMI**, **cholesterol**, **age**).  
- Perform **multivariate regression** to predict BP from HbA1c and other features.  
- Apply **feature scaling** and **PCA** for dimensionality reduction.  

---

## Author
**Leila (Faezeh) Gerayeli**  
Biomedical Engineer | Aspiring Data Scientist  
leila.gerayeli@gmail.com  
[LinkedIn](https://www.linkedin.com/in/leila-gerayeli-a8148b59/) | [GitHub](https://github.com/LeilaBioMed)

---

*This project is part of my portfolio to demonstrate data exploration and visualization skills applied to biomedical datasets.*

---

## How to Use

Clone this repository:
```bash
git clone https://github.com/LeilaBioMed/Synthetic_Biomedical_Dataset_EDA.git
cd biomedical-eda

