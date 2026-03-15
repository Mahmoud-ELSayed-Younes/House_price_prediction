![Python](https://img.shields.io/badge/Python-3.10-blue)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-green)
![License](https://img.shields.io/badge/License-MIT-yellow)
# 🏠 Boston House Price Prediction

This project builds a machine learning model to predict housing prices in Boston using **XGBoost Regressor**.  
The model analyzes socio-economic and environmental factors to estimate the **median value of owner-occupied homes**.

---

# 📊 Dataset

The dataset contains:

- **506 observations**
- **13 features**
- **Target Variable:** `PRICE` (Median value of homes in $1000s)

---

# 🔎 Exploratory Data Analysis (EDA)

Before training the model, an Exploratory Data Analysis was conducted to understand relationships between features.

## Key Insights

- **RM (Average Rooms per Dwelling)**  
  Strong **positive correlation** with house prices.  
  More rooms → higher house value.

- **LSTAT (% Lower Status Population)**  
  Strong **negative correlation** with house prices.

- **PTRATIO (Pupil-Teacher Ratio)**  
  Higher ratios tend to correlate with **lower housing prices**.

---

# 📈 Correlation Between Features

![Correlation Matrix](Images/cheatmap%20to%20understand%20correlation.png)

---

# ⚙️ Project Workflow

### 1️⃣ Data Preprocessing
- Loaded Boston dataset
- Checked for missing values
- Cleaned and validated dataset

### 2️⃣ Exploratory Data Analysis
- Distribution plots
- Correlation heatmap
- Multicollinearity inspection

### 3️⃣ Feature Engineering
- Train/Test split  
- **80% Training**
- **20% Testing**

### 4️⃣ Modeling

Model used:

**XGBoost Regressor**

Hyperparameters:
n_estimators = 100
max_depth = 2


---

# 📊 Model Performance

| Metric | Training Set | Test Set |
|------|------|------|
| R² Score | 0.976 | 0.916 |
| MAE | 1.092 | 1.928 |

The model explains **over 91% of the variance** in the test data.

---

# 📉 Actual vs Predicted Prices

![Actual vs Predicted](Images/Actual%20Price%20vs%20Predicted%20price.png)

---

# 📐 R² Formula

The R² score is calculated as:

R² = 1 - (SS_res / SS_tot)

---
# 🛠 Tech Stack

**Language**

- Python

**Libraries**

- NumPy
- Pandas
- Matplotlib
- Seaborn

**Machine Learning**

- Scikit-learn
- XGBoost

---

# 🚀 How to Run

```bash
git clone https://github.com/yourusername/boston-house-price-prediction.git

cd boston-house-price-prediction

pip install -r requirements.txt

