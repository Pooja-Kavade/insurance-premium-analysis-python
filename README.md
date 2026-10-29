# Insurance Premium Analysis

Exploratory Data Analysis (EDA) of an insurance premium dataset using Python. The project examines how customer demographics and risk factors relate to insurance costs.

---

## Project Overview

This notebook analyzes **1,338 customer records** from `Insurance Premium.csv` to understand:

- Customer demographics (age, gender, region)
- Risk attributes (BMI, smoking status, number of children)
- How these factors relate to **annual insurance premium**

The analysis focuses on data quality, descriptive statistics, and visualizations. It does **not** include predictive modeling (that is listed under next steps).

---

## Dataset

| Attribute | Details |
|-----------|---------|
| **Source file** | `Insurance Premium.csv` |
| **Rows** | 1,338 |
| **Original columns** | 8 |
| **Columns after cleaning** | 7 (ID dropped) |
| **Missing values** | 0 |

### Features

| Feature | Type | Description |
|---------|------|-------------|
| **Age** | Numeric | Age of the primary beneficiary (18–64) |
| **Gender** | Categorical | Male / Female |
| **BMI** | Numeric | Body Mass Index (15.96 – 53.13) |
| **Children** | Numeric | Number of dependents (0–5) |
| **Smoker** | Categorical | Yes / No |
| **Region** | Categorical | East / South / West / North |
| **Premium** | Numeric (Target) | Annual insurance premium charged |

---

## Tools & Libraries

```python
numpy
pandas
matplotlib
seaborn
```

---

## Analysis Steps

### 1. Data Loading
- Load CSV into a pandas DataFrame
- Display first 5 rows and dataset shape

### 2. Data Quality Check
- Check for missing (null) values → **none found**
- Review data types with `df.info()`
- Separate categorical (string) columns

### 3. Descriptive Statistics
- Summary stats for numerical columns (`describe()`)
- Value counts for Gender, Smoker, and Region
- Drop the non-informative `ID` column

### 4. Visualizations
| Chart | Purpose |
|-------|---------|
| **Gender count plot** | Compare number of male vs female customers |
| **Premium pie charts** | Share of total premium by Gender, Smoker, and Region |
| **Correlation heatmap** | Relationships among Age, BMI, Children, and Premium |

---

## Key Findings

| Insight | Detail |
|---------|--------|
| **Clean data** | No missing values; ready for analysis after dropping ID |
| **Gender balance** | Male ≈ 50.5% (676), Female ≈ 49.5% (662) |
| **Smoking minority** | ~20.5% smokers (274), but they drive a large share of total premium |
| **Regions** | Roughly equal split across East, South, West, North |
| **Age** | Mean ≈ 39.2 years (range 18–64) |
| **BMI** | Mean ≈ 30.7 (overweight range on average) |
| **Premium** | Mean ≈ $13,270; high variance (std ≈ $12,110); max $63,770 |
| **Correlations** | Positive links between Age–Premium and BMI–Premium; weaker for Children |

---

## How to Run

1. Place `Insurance Premium.csv` in an accessible path (update the path in the notebook if needed).
2. Open the Jupyter notebook:

```bash
jupyter notebook insurance_python.ipynb
```

3. Run cells in order from top to bottom.

> **Note:** The original notebook uses a Windows path:
> `C:\Users\ATUL\Downloads\Insurance Premium.csv`  
> Change this to your local path before running.

---

## Project Structure

```
.
├── insurance_python.ipynb   # Main analysis notebook
├── Insurance Premium.csv    # Source dataset
└── README.md                # This file
```

---

## Recommended Next Steps

1. **Feature engineering** — Encode categoricals; create age/BMI bands  
2. **Train/test split** — Prepare data for supervised learning  
3. **Build models** — Linear Regression, Random Forest, XGBoost  
4. **Evaluate** — Compare RMSE, MAE, and R² on a held-out test set  
5. **Interpret** — Use feature importance or SHAP values for pricing insight  

---

## Author

Python Data Analysis Project — Insurance Premium EDA
