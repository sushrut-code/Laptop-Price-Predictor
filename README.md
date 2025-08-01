# Laptop-Price-Predictor
This project uses various models and compares them on the basis of their ability to predict the price of the laptop.

📌 Project Overview
This project predicts the price of a laptop based on its specifications using multiple regression models.
We perform data preprocessing, feature engineering, exploratory data analysis (EDA), model training, and model selection to build the most accurate price prediction pipeline.

The dataset contains various features of laptops such as company, type, CPU, GPU, RAM, storage, operating system, weight, display resolution, etc.
The goal is to predict the log-transformed price of a laptop, providing reliable estimates for unseen configurations.

📂 Dataset
Source: laptop_data.csv (CampusX dataset)

Rows: 1303

Columns: 12 (after preprocessing: 14+ engineered features)

Target Variable: Price (continuous numerical)

Features:
Categorical: Company, TypeName, Cpu, Gpu, OpSys

Numerical: Inches, Ram, Weight, Storage capacities (HDD, SSD)

Engineered: Touchscreen, IPS panel, PPI (pixels per inch), CPU brand, GPU brand, OS category

🛠️ Tech Stack
Language: Python 3.x

Libraries:

pandas, numpy

matplotlib, seaborn

scikit-learn

xgboost (optional)

pickle (for model saving)

🔑 Key Steps
Data Cleaning

Removed duplicates, handled missing values

Converted RAM and weight to numeric

Parsed screen resolution, CPU, GPU, and memory columns

Feature Engineering

Extracted:

Touchscreen and IPS flags

PPI = screen pixel density

CPU brand, GPU brand, OS category

HDD, SSD sizes from combined memory column

EDA

Distribution plots for price and numeric features

Bar plots showing average prices by brand, type, CPU, OS

Correlation heatmap for numerical features

Model Training

Models tested:

Linear Regression, Ridge, Lasso

Decision Tree, KNN, SVR

Random Forest, Extra Trees, AdaBoost, Gradient Boosting

XGBoost (if installed)

Pipeline with:

ColumnTransformer → OneHotEncoder for categorical features

Regression model

Model Evaluation

Metrics:

R² Score

Mean Absolute Error (MAE)

Best model: Random Forest Regressor

R²: 0.8873

MAE: 0.1586

Model Saving

df.pkl: Processed dataset

pipe.pkl: Trained pipeline (best model)
