# Overview
This project aims to determine whether survey questions can effectively predict diabetes status. It compares different machine learning models and evaluates their performance using metrics like accuracy, recall, and feature importance. The goal is to find the best model for predicting diabetes while minimizing false negatives.

## Dataset
- **Source**: CDC survey data for binary classification of diabetes status.
- **Target Variable**: `Diabetes_binary` (0 = No Diabetes, 1 = Diabetes or Prediabetes).
- **Features**:
  - Health indicators like BMI, physical activity, and cholesterol levels.
  - Demographic data such as age, sex, and income.
  - Behavioral factors like smoking status and alcohol consumption.

## Data Preprocessing
- Handling missing values using `SimpleImputer` with mean strategy.
- Feature scaling using `StandardScaler`.
- Outlier removal for `BMI`, `MentHlth`, and `PhysHlth` to improve model performance.
- Mapping categorical values to more human-readable labels for better data understanding.

## Project Structure

```
├── diabetes_binary_classification_data.csv 
├── diabetes_prediction.ipynb
├── README.md
└── requirements.txt
```                       

## Models Used
The following machine learning models were implemented and compared:
- **Logistic Regression**: Baseline model with feature scaling for better convergence.
- **Decision Tree Classifier**: Non-linear model that can capture interactions between features.
- **Random Forest Classifier**: Ensemble method providing feature importance and robustness.

## Results and Evaluation
The models were evaluated using metrics like accuracy, recall, and confusion matrix to assess their ability to correctly identify diabetes cases:

- **Logistic Regression**:
  - Accuracy: 87.01%
  - Recall: 11.09% (struggles to capture diabetes cases)
  
- **Decision Tree**:
  - Accuracy: 79.02%
  - Recall: 30.08% (better at identifying diabetes but less overall accuracy)

- **Random Forest**:
  - Accuracy: 86.76%
  - Recall: 7.52% (strong for majority class, weak for diabetes detection)

## Feature Importance
Top factors contributing to diabetes prediction include:
- **BMI**: Strongest predictor of diabetes.
- **Age**: Older individuals have higher diabetes risk.
- **Physical Health**: Chronic conditions impact diabetes risk.

## Recommendation
- **Best Model**: Logistic Regression.
- **Additional Features**: Consider adding family history for better predictions.
