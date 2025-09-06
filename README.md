## Wild Blueberry Yield Prediction

### Project Overview

This project aims to predict the **yield of wild blueberries** based on various environmental and pollination-related factors. By analyzing features such as clone size, honeybee and bumblebee population sizes, temperature ranges, and fruit-related metrics, the goal is to develop a regression model that can accurately forecast blueberry yield. This is a crucial task for agricultural planning and crop management.

-----

### Technical Highlights

  * **Dataset**: The dataset used is `WildBlueberryPollinationSimulationData.csv`, which contains simulated data for wild blueberry pollination.
  * **Size**: 777 entries, 18 columns.
  * **Key Features**:
      * **Pollination**: `clonesize`, `honeybee`, `bumbles`, `andrena`, `osmia`.
      * **Environment**: `MaxOfUpperTRange`, `MinOfUpperTRange`, `AverageOfUpperTRange`, `MaxOfLowerTRange`, `MinOfLowerTRange`, `AverageOfLowerTRange`, `RainingDays`, `AverageRainingDays`.
      * **Fruit Metrics**: `fruitset`, `fruitmass`, `seeds`.
  * **Approach**:
      * **Data Cleaning**: The `Row#` column was dropped as it is an irrelevant index. The dataset was clean with no missing values or duplicates.
      * **Exploratory Data Analysis**: Histograms, box plots, scatter plots, and a heatmap were used for visualization to understand data distributions and feature relationships.
      * **Data Scaling**: `MinMaxScaler` was applied to all feature columns to bring them to a common scale.
      * **Regression Task**: The target variable is `yield`.
      * **Models Used**:
          * A suite of regression models were trained, including Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN).
  * **Best R² Score**:
      * **0.991** with Gradient Boosting Regressor.
      * **0.989** with XGBoost Regressor.
      * **0.988** with Ridge Regressor.
      * The extremely high R² scores for multiple models indicate that the input features are highly predictive of wild blueberry yield.

-----

### Purpose and Applications

  * Enable farmers and agronomists to **predict blueberry yield** for better crop planning.
  * Optimize pollination strategies by understanding the impact of different bee populations.
  * Support data-driven decision-making in agricultural management, from irrigation to pest control.
  * Provide a foundational model for research on the complex interplay between environmental factors and crop production.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Wild-Blueberry-Yield-Prediction.git
cd Wild-Blueberry-Yield-Prediction
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for the top-performing regression models.
  * Investigating the impact of the data scaling and feature selection steps.
  * Adding explainability (e.g., SHAP or LIME) to understand which environmental and pollination factors are the most significant drivers of yield.
