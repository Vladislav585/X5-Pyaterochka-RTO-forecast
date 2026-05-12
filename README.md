# Retail Revenue (RTO) Prediction for Pyaterochka Stores (X5 Group)

This repository contains a high-performance machine learning solution for predicting the monthly retail turnover (RTO) of "Pyaterochka" stores. The project was developed as part of a data science hackathon.

## 📌 Project Overview
**Objective:** Develop a model to predict the total revenue for over 20,000 stores for November 2023 based on historical sales data and store characteristics.
**Metric:** MAPE (Mean Absolute Percentage Error).
**Final Performance:** 
*   **MAPE:** 4.01% 
*   **Hackathon Score:** 95.99 / 100

## 🛠 Tech Stack
*   **Core:** Python, Pandas, NumPy
*   **ML Framework:** CatBoost (Gradient Boosting on Decision Trees)
*   **Validation:** 5-Fold Cross-Validation (K-Fold)
*   **Pre-processing:** Scikit-learn

## 🚀 Key Features & Engineering
To achieve a top-tier score, we implemented an extensive feature engineering pipeline:

1.  **Target Transformation:** Used `log1p` transformation on the revenue data to stabilize variance and directly optimize the model for percentage-based error (MAPE).
2.  **Temporal Features (Lags):** 
    *   Short-term lags (1, 2, 3 months) to capture recent dynamics.
    *   Long-term lags (6, 9 months) to account for seasonal trends.
3.  **Cyclical Time Encoding:** Encoded months using Sine and Cosine transformations (`month_sin`, `month_cos`) to preserve the cyclical nature of the calendar year.
4.  **Economic Efficiency Metrics:**
    *   Revenue per square meter (`rto_per_area`).
    *   Revenue per checkout counter (`rto_per_kassa`).
    *   Momentum indicators (e.g., current month vs. 6-month average).
5.  **Regional Benchmarking:** Integrated regional average revenue to provide the model with geographical context.

## 📈 Model Performance
The model utilizes a **CatBoostRegressor** with fine-tuned hyperparameters (learning rate, depth, L2 regularization) and early stopping to prevent overfitting. The 5-fold CV strategy ensured the model generalizes well to unseen store data.

## 👥 Contributors
This project was a collaborative effort by:
*   **Vladislav** ([@Vladislav585](https://github.com/Vladislav585))
*   **KremlevLev** ([@FriendGitHubUsername](https://github.com/KremlevLev)) — *Collaborated on feature engineering and model tuning.*

## 📂 Repository Structure
*   `x5-rto.py`: The main script for data processing, training, and inference.
*   `test.csv`: Final prediction file for November.
*   `README.md`: Project documentation.

## ⚙️ Usage
1. Install dependencies:
   ```bash
   pip install catboost pandas numpy scikit-learn
   ```
2. Run the solution:
   ```bash
   python solution.py
   ```

______________________________________________________________________________________________________________________________________________________________________________________________________


Вот профессиональный вариант **README.md** на английском языке. Я добавил специальный раздел **"Contributors"**, где ты сможешь указать своего друга.

---

# Retail Revenue (RTO) Prediction for Pyaterochka Stores (X5 Group)

This repository contains a high-performance machine learning solution for predicting the monthly retail turnover (RTO) of "Pyaterochka" stores. The project was developed as part of a data science hackathon.

## 📌 Project Overview
**Objective:** Develop a model to predict the total revenue for over 20,000 stores for November 2023 based on historical sales data and store characteristics.
**Metric:** MAPE (Mean Absolute Percentage Error).
**Final Performance:** 
*   **MAPE:** 4.01% 
*   **Hackathon Score:** 95.99 / 100

## 🛠 Tech Stack
*   **Core:** Python, Pandas, NumPy
*   **ML Framework:** CatBoost (Gradient Boosting on Decision Trees)
*   **Validation:** 5-Fold Cross-Validation (K-Fold)
*   **Pre-processing:** Scikit-learn

## 🚀 Key Features & Engineering
To achieve a top-tier score, we implemented an extensive feature engineering pipeline:

1.  **Target Transformation:** Used `log1p` transformation on the revenue data to stabilize variance and directly optimize the model for percentage-based error (MAPE).
2.  **Temporal Features (Lags):** 
    *   Short-term lags (1, 2, 3 months) to capture recent dynamics.
    *   Long-term lags (6, 9 months) to account for seasonal trends.
3.  **Cyclical Time Encoding:** Encoded months using Sine and Cosine transformations (`month_sin`, `month_cos`) to preserve the cyclical nature of the calendar year.
4.  **Economic Efficiency Metrics:**
    *   Revenue per square meter (`rto_per_area`).
    *   Revenue per checkout counter (`rto_per_kassa`).
    *   Momentum indicators (e.g., current month vs. 6-month average).
5.  **Regional Benchmarking:** Integrated regional average revenue to provide the model with geographical context.

## 📈 Model Performance
The model utilizes a **CatBoostRegressor** with fine-tuned hyperparameters (learning rate, depth, L2 regularization) and early stopping to prevent overfitting. The 5-fold CV strategy ensured the model generalizes well to unseen store data.

## 👥 Contributors
This project was a collaborative effort by:
*   **Vladislav** ([@Vladislav585](https://github.com/Vladislav585))
*   **KremlevLev** ([@FriendGitHubUsername](https://github.com/KremlevLev)) — *Collaborated on feature engineering and model tuning.*

## 📂 Repository Structure
*   `solution.py`: The main script for data processing, training, and inference.
*   `test.csv`: Final prediction file for November.
*   `README.md`: Project documentation.

## ⚙️ Usage
1. Install dependencies:
   ```bash
   pip install catboost pandas numpy scikit-learn
   ```
2. Run the solution:
   ```bash
   python solution.py
   ```
