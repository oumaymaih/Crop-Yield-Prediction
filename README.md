# Crop Yield Prediction

## Project Overview
This project aims to predict agricultural crop yield using machine learning regression models.  
The goal is to support decision-making in agriculture by providing accurate yield predictions based on environmental and agricultural factors.

---

## Dataset
The dataset used in this project is a public dataset from Kaggle:

Title : **Agricultural Crop Yield in Indian States Dataset** 
Link : https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fakshatgupta7%2Fcrop-yield-in-indian-states-dataset

It contains agricultural data from different states in India between 1997 and 2020.

It is included in the `data/` folder for reproducibility.

### Features:
- Area (cultivated land in hectares)
- Annual Rainfall (mm)
- Fertilizer (kg)
- Pesticide (kg)
- Crop Year
- Crop Type
- Season
- State

### Target:
- Yield (crop production per unit area)

---

## Technologies Used
- Python
- Pandas & NumPy → data manipulation
- Matplotlib & Seaborn → data visualization
- Scikit-learn → preprocessing, modeling, evaluation

---

## Project Workflow

### 1. Data Understanding
- Dataset exploration (types, distributions, statistics)
- Identification of potential data leakage (removal of "Production")

### 2. Data Preprocessing
- Handling missing values (median & most frequent imputation)
- Log transformation (features + target)
- Feature scaling (StandardScaler)
- Encoding categorical variables (One-Hot Encoding)

### 3. Modeling Approach
A progressive modeling strategy was adopted:

#### Baseline Models:
- Linear Regression
- KNN Regressor
- Decision Tree

#### Advanced Models:
- Random Forest Regressor
- Voting Regressor

### 4. Validation Strategy
- 5-fold cross-validation
- Evaluation metrics:
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)
  - R² Score

---

## Results

### Final Model: Random Forest Regressor

| Metric |  Value  |
|------  |---------|
| RMSE   | 120.654 |
| MAE    | 8.649   |
| R²     | 0.982   |

### Interpretation:
- **High R² (0.982)** → excellent explanatory power
- **Low MAE** → accurate predictions in most cases
- **Higher RMSE** → presence of some extreme prediction errors

---

## Key Insights
- The problem is **non-linear**, making ensemble models more effective
- Random Forest significantly improves performance over baseline models
- Agricultural yield depends on complex interactions between variables

---

## Conclusion
Despite the presence of outliers and skewed distributions, the use of ensemble learning methods combined with proper preprocessing and cross-validation resulted in a highly accurate and robust model.

The model demonstrates strong generalization ability and can be effectively used to support agricultural decision-making.

---

## Future Improvements
- Hyperparameter tuning (GridSearch / RandomSearch)
- Integration of additional features (soil quality, temperature)
- Model deployment (web app or API)
- Testing on local (Moroccan) agricultural data

---

## Note
The notebook is written in French, but the methodology, code, and results are clearly structured and easy to understand.

