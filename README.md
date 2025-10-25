# Predictive Maintenance for Wind Turbines using Machine Learning

## Project Overview
This project focuses on **predicting generator failures in wind turbines** using sensor-based data. By building and tuning various classification models (Decision Tree, Random Forest, Gradient Boosting, AdaBoost, XGBoost), the goal is to **identify potential failures before they occur**, reducing maintenance and replacement costs.

## Dataset
The dataset is provided by **ReneWind**, a company working on wind turbine efficiency. The data is a ciphered version of real sensor readings to protect confidentiality.

- **train.csv** – For training and tuning models.
- **test.csv** – For evaluating the performance of the final model.
- **Predictors**: 40 sensor-based features.
- **Target**: `1` indicates a failure, `0` indicates no failure.

> **Note:** Repairing a generator is cheaper than replacing it, and inspection costs are less than repair costs. Correctly predicting failures is critical for cost reduction.

## Objective
- Build and tune classification models to predict turbine generator failures.  
- Handle **imbalanced data** using **oversampling and undersampling** techniques to improve model recall.  
- Evaluate models using **accuracy, recall, precision, and F1-score** across **train, validation, and test sets**.  
- Perform **feature importance analysis** to identify key predictors.

## Models Implemented
- **Decision Tree Classifier**  
- **Random Forest Classifier**  
- **Gradient Boosting Classifier**  
- **AdaBoost Classifier**  
- **XGBoost Classifier**  

## Imbalanced Data Handling
- **Oversampling:** Increases minority class samples to balance the dataset.  
- **Undersampling:** Reduces majority class samples to balance the dataset.  
- Models were trained on both oversampled and undersampled datasets to compare performance.

## Model Performance Comparison
- Metrics compared include **Accuracy, Recall, Precision, and F1-score**.  
- **Recall** is prioritized to minimize undetected failures (false negatives), as these are costlier than false positives.  
- Feature importance analysis highlights the most critical turbine sensors for predicting failures.

## Model Building: XGBoost with Oversampled Data
XGBOOST on oversampled data worked best!
To handle the class imbalance in the wind turbine failure dataset, the training data was oversampled. An **XGBoost classifier** was then trained using a pipeline that includes:

- **Preprocessing:** Column transformations for numerical features (imputation + scaling).
- **Model:** XGBoost with tuned hyperparameters
 
The model was evaluated on **train, validation, and test sets** using metrics such as Accuracy, Recall, Precision, and F1-score. Feature importance was also extracted to identify key turbine sensor predictors affecting failures.

## Usage
1. Clone the repository:

git clone https://github.com/mariyamzx/Predictive-maintenance-for-Wind-Turbines-using-ML.git
## Install dependencies:

pip install -r requirements.txt
Open the Jupyter notebook (wind_turbine_analysis.ipynb) to explore the data, train models, handle imbalanced datasets, and compare model performance.

## Author

**Mariyam Muzammil** 
[GitHub](https://github.com/mariyamzx)
