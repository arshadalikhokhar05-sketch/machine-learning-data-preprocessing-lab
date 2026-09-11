# Lab 05 — Linear Regression: Predicting House Prices

## 📌 Project Overview
This repository contains the implementation and analysis for **Lab 05: Linear Regression**. The primary objective is to build a multiple linear regression model using `scikit-learn` to predict residential home transaction prices (`SalePrice`) based on property features, room counts, and structural conditions.

- **Dataset:** [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)
- **Model:** Multiple Linear Regression (`sklearn.linear_model.LinearRegression`)
- **Target Variable:** `SalePrice`

---

## 👤 Author Information
- **Name:** Arshad Ali Khokhar
- **Student ID:** 05
- **Program:** BSCS 5th Semester
- **GitHub:** [arshadalikhokhar05](https://github.com/arshadalikhokhar05)
- **Kaggle:** [arshadalikhokhar05](https://www.kaggle.com/arshadalikhokhar05)

---

## 🛠️ Key Steps & Methodology

1. **Exploratory Data Analysis (EDA):**
   - Analyzed 1,460 rows and 81 features.
   - Summarized target variable distribution (`SalePrice` mean: ~$180,921).

2. **Feature Selection & Preprocessing:**
   - **Numerical Features Selected:** `GrLivArea`, `OverallQual`, `YearBuilt`, `TotalBsmtSF`, `FullBath`, `GarageCars`, `LotArea`
   - **Categorical Features Selected:** `CentralAir`, `KitchenQual`, `Neighborhood`, `HouseStyle`
   - **Encoding:**
     - Ordinal Mapping: `KitchenQual` (`Ex: 4` to `Po: 0`)
     - Binary Encoding: `CentralAir` (`Y: 1`, `N: 0`)
     - One-Hot Encoding: `Neighborhood` and `HouseStyle` (using `drop_first=True`)

3. **Model Training & Evaluation:**
   - **Data Split:** 80% Training / 20% Testing (`random_state=42`)
   - **Performance Metrics (Test Set):**
     - **MAE:** $22,343.43
     - **RMSE:** $35,425.36
     - **R² Score:** 0.8364 (explains ~83.6% of price variance)

4. **Residual Analysis:**
   - Evaluated prediction residual normality and scatter distribution across predicted prices.

5. **Kaggle Submission:**
   - Generated `submission.csv` on unseen test data (`test.csv`).
   - Achieved a Kaggle Public Leaderboard Score of **0.20140**.

---

## 📁 Repository Structure

```text
.
├── lab5_Arshad_Ali_Khokhar_house_price.ipynb   # Completed Lab 5 Notebook
├── submission.csv                               # Kaggle Test Predictions
├── train.csv                                    # Kaggle Training Dataset
├── test.csv                                     # Kaggle Test Dataset
└── README.md                                    # Lab Overview & Documentation
