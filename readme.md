# 🚗 Diesel Vehicle Emission Prediction and EURO 4 Compliance Checker


## 📌 Project Overview
This project aims to predict emission values from diesel vehicles and determine their compliance with EURO 4 standards using machine learning models. The work is based on a small dataset containing vehicle model names and associated emission metrics.

---

## 🎯 Objectives
- Predict the following emissions:
  - `CO(%)`
  - `CO2(%)`
  - `O2(%)`
  - `NOX (ppm)`
- Determine EURO 4 `Pass`/`Fail` compliance via rule-based thresholding

---

## 📂 Dataset Summary
- Format: Excel (`.xlsx`)
- Key Columns:
  - `Model of vehicle`
  - `CO(%)`
  - `CO2(%)`
  - `O2(%)`
  - `NOX (ppm)`
  - `EURO 4 (Pass/Fail)`
- Approximate Rows: 25 (small sample)

---

## 🛠️ Tech Stack
- Python 3.x
- Libraries:
  - `pandas`, `numpy` for data handling
  - `scikit-learn` for modeling
  - `matplotlib`, `seaborn` for visualization

---

## 📈 Project Workflow

### 1. Data Exploration
- Cleaned and renamed columns
- Dropped missing values
- Visualized distributions and correlations

### 2. Preprocessing
- Encoded vehicle model names using `LabelEncoder`
- Scaled input features using `StandardScaler`
- Defined multiple target variables for regression

### 3. Model Training
Two models were trained and evaluated:

#### 🔹 Linear Regression
- R² Score: **-0.15**
- RMSE: **37.48**
- Result: Poor fit due to linearity and small data

#### 🔸 Random Forest Regressor
- R² Score: **0.13**
- RMSE: **26.30**
- Result: Better performance and chosen as final model

### 4. Emission Prediction & Compliance
- Emissions predicted based on new input vehicle models
- EURO 4 compliance assessed using 75th percentile thresholds

---

## 🚀 Future Improvements
- Expand dataset (more rows, more features: engine size, mileage, etc.)
- Train a classifier for `EURO 4` prediction directly
- Build an interactive app using `Streamlit` or an API using `FastAPI`
- Tune hyperparameters for better performance

---

## 💻 Installation

```bash
# Create virtual environment
python -m venv .venv

# Activate virtual environment (Windows)
.venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

## 👤 Author
**Mayomikun Joshua Fiki**  
July 2025
