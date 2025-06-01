# Project: Delhi Rental Price Prediction Model

## Overview

This project represents a practical application of data science principles to engineer a predictive model for residential rental prices in Delhi. It was undertaken to demonstrate skills in data analysis, technological implementation, and methodical research to derive actionable insights from complex datasets. The work showcases the application of knowledge from academic coursework and a Data Analytics certification to identify and understand market dynamics. This endeavor serves as a comprehensive exploration into the factors governing rental valuations within a major metropolitan area, translating raw data into a functional predictive tool.

## Problem Statement

The core objective was to dissect the key market factors influencing rental prices within Delhi and to construct a reliable predictive model for price estimation. This addresses the common challenge of navigating an often opaque and rapidly changing rental market, providing a data-driven approach to price assessment. The aim is to empower stakeholders—tenants, landlords, and analysts—with a clearer understanding of price structures, fostering more informed decision-making in the Delhi rental ecosystem.

## Dataset

*   **Source:** The dataset utilized was sourced from Kaggle, originating from a third-party compilation. (Specifically, the `mkd.csv` file, as detailed in the associated technical report and notebook).
*   **Origin:** Data was initially gathered by scraping housing information from Makaan.com, a significant Indian real estate portal. This scraped data, focused on Delhi rental properties and their associated market factors (such as `Size`, `Location`, `Area_sqft`, `Property_type`, `Bathroom` count, and `Status`), formed the basis of the Kaggle dataset used for this analysis. The target variable was `Rent_price`.

## Methodology

A structured, systematic approach was employed for model development, mirroring the detailed workflow presented in the accompanying technical report and Jupyter notebook:

1.  **Data Acquisition & Initial Inspection:** Utilized the pre-compiled Kaggle dataset (`mkd.csv`). Initial steps involved loading the data, understanding its structure, dimensions, data types, and performing a preliminary assessment of missing values and basic statistics.
2.  **Data Preprocessing & Cleaning:** Employed Python and its associated data science libraries (Pandas, NumPy) for thorough data cleaning. This included:
    *   Handling duplicate entries.
    *   Removing irrelevant features (`Seller_name`, `Security_deposit` due to target leakage).
    *   Correcting data errors (e.g., `Size == 0`).
    *   Normalizing the target variable (`Rent_price`) from string to numeric.
    *   Imputing missing values in numerical features (using KNNImputer) and categorical features (e.g., `Facing_direction` filled with "Unknown").
    *   Harmonizing categorical values and ensuring correct data types.
3.  **Exploratory Data Analysis (EDA):** Conducted in-depth exploratory analysis using Matplotlib and Seaborn to identify patterns, variable relationships, distributions (including skewness of `Rent_price`), and correlations. This phase was crucial for preparing the data for robust modeling and understanding its inherent characteristics.
4.  **Feature Engineering & Transformation:**
    *   Separated features (X) and target (y).
    *   Performed a train-test split.
    *   Applied `CatBoostEncoder` for high-cardinality 'Location' and `OneHotEncoder` for other categoricals.
    *   Scaled numerical features using `StandardScaler`.
5.  **Predictive Modeling & Evaluation:** Developed and evaluated a suite of predictive models using Python (Scikit-learn, XGBoost, Category Encoders) to forecast rental prices. This involved:
    *   Training models like Linear Regression, Ridge, Lasso, Decision Tree, Random Forest, Gradient Boosting, SVR, MLP, and XGBoost.
    *   Evaluating models based on MAE, RMSE, and R2 scores.
    *   Performing hyperparameter tuning (GridSearchCV) for top-performing tree-based models.
    *   Conducting a comparative experiment by modeling the log-transformed target variable.
    The process emphasized identifying significant predictors and understanding underlying trends within the Delhi rental market based on the empirical data.

## Key Findings & Deliverables

The project resulted in the following concrete outcomes, as detailed in the technical report:

*   **Identification of significant trends and influential factors:** `Area_sqft`, `Location` (CatBoostEncoded), and `Bathroom` count were identified as primary drivers of rental prices in the Delhi market.
*   **Development of a functional predictive model:** Tree-based ensemble models, particularly Random Forest (Test R2 ≈ 0.9020), demonstrated strong predictive capability for estimating rental prices based on property attributes.
*   **A comprehensive report:** Detailing methodologies, data cleaning steps, EDA insights, feature engineering techniques, model selection, evaluation metrics, hyperparameter tuning, comparative experiment results, and conclusions.
*   **Creation of clear data visualizations:** (Using Matplotlib and Seaborn) to communicate data distributions, relationships, model performance comparisons, and feature importances effectively. These are embedded within the technical report and the Jupyter notebook.
*   **Saved Model:** The best performing model (Random Forest) was serialized using `joblib` for potential future use or deployment.

## Technologies Utilized

The following tools and technologies were instrumental to the project's execution:

*   **Programming Language:** Python
*   **Core Libraries:**
    *   **Pandas & NumPy:** For data manipulation, cleaning, and numerical operations.
    *   **Matplotlib & Seaborn:** For data visualization and exploratory data analysis.
    *   **Scikit-learn:** For building and evaluating predictive machine learning models, preprocessing, and metrics.
    *   **Category Encoders:** For `CatBoostEncoder`.
    *   **XGBoost:** For the XGBoost regression model.
    *   **Joblib:** For model persistence.
*   **Development Environment:** Jupyter Notebook

## Project Status

*   Academic Project – Completed. 

## Contact

*   Email: pagarani07@gmail.com
