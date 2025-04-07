# Energy Efficiency Dataset Analysis (Kelompok 6)

This project is a comprehensive analysis of the [Energy Efficiency Data Set](https://archive.ics.uci.edu/ml/datasets/Energy+efficiency) from the UCI Machine Learning Repository. It aims to predict the **Heating Load (Y1)** and **Cooling Load (Y2)** of buildings based on several architectural and environmental features.

## 📊 Project Overview

- **Dataset Source:** UCI Machine Learning Repository
- **Total Instances:** 768
- **Features:** 8
  - Relative Compactness (X1)
  - Surface Area (X2)
  - Wall Area (X3)
  - Roof Area (X4)
  - Overall Height (X4)
  - Orientation (X6)
  - Glazing Area (X7)
  - Glazing Area Distribution (X8)
- **Targets:**
  - Heating Load (Y1)
  - Cooling Load (Y2)

## 🛠️ Tools & Libraries Used

- Python
- Pandas
- NumPy
- Seaborn & Matplotlib
- Scikit-learn

## 🧪 Workflow Summary

### 1. Data Understanding
- Reviewed dataset attributes and structure.
- Identified that `Overall Height` and `Relative Compactness` are perfectly negatively correlated.

### 2. Data Preprocessing
- Removed `Overall Height` due to perfect multicollinearity.
- Applied one-hot encoding to categorical variables (Orientation, Glazing Area Distribution).
- Normalized features using Min-Max scaling.

### 3. Exploratory Data Analysis (EDA)
- Visualized correlations using heatmaps.
- Detected outliers and distribution patterns using boxplots and pairplots.

### 4. Model Building

#### a. Linear Regression
- Built separate linear regression models for Y1 and Y2.
- Evaluated using MSE, MAE, and R² scores.

#### b. Polynomial Regression (Degree = 3)
- Transformed features using `PolynomialFeatures`.
- Observed improved model performance with non-linear relationships.

### 5. Evaluation Metrics
Used the following metrics for both targets:
- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

## 📈 Results Summary

| Model Type         | Target | MSE     | MAE     | R² Score |
|--------------------|--------|---------|---------|----------|
| Linear Regression  | Y1     | ~6.57   | ~1.96   | ~0.92    |
| Polynomial (deg=3) | Y1     | ~1.06   | ~0.62   | ~0.99    |
| Linear Regression  | Y2     | ~9.57   | ~2.34   | ~0.96    |
| Polynomial (deg=3) | Y2     | ~2.35   | ~1.03   | ~0.99    |

> Polynomial regression significantly improved the model accuracy for both Heating and Cooling Load prediction.

## 👥 Contributors

This project was developed as part of a group assignment in a data analysis course:

- **Group 6 Members**
  1. Alhusna Hanifah (2208107010060)
  2. Farhanul Khair (2208107010076)
  3. Iffatun Nisa Nasrullah (2208107010009)
  4. M. Bintang Indra Hidayat (2208107010023)
  5. Qandila Ahmara (2208107010039)


