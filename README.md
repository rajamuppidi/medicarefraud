# Medicare Fraud Detection

## Overview

The Medicare Fraud Detection project aims to identify fraudulent healthcare providers through data analysis and machine learning. By analyzing healthcare insurance claims data, the project seeks to detect patterns and anomalies indicative of fraudulent activities. This initiative is crucial for reducing financial losses, protecting patient care, and promoting a more secure and equitable healthcare system.

## Problem Statement

The healthcare industry faces significant challenges due to providers submitting false claims for services not rendered or inflating the costs of services provided. This fraudulent activity leads to substantial financial losses for insurers and government programs, compromising patient care and increasing healthcare costs.

## Solution

Our solution involves developing a predictive model using machine learning to analyze insurance claims data and identify potential fraud. Early detection of fraudulent claims helps mitigate financial losses, benefits insurers and taxpayers, and strengthens the integrity of the healthcare system.

## Datasets

The datasets used in this project are sourced from Kaggle and include:

- **Training Labels Dataset**: Identifies providers suspected of fraud.
- **Beneficiary Details Dataset**: Provides demographic and health-related information.
- **Inpatient Claims Dataset**: Records of inpatient services billed to insurance.
- **Outpatient Claims Dataset**: Details of outpatient services billed to insurance.

## Data Analysis

### Exploratory Data Analysis (EDA)

- Histograms for annual reimbursement and deductible amounts for inpatient (IP) and outpatient (OP) services.
- Distribution histograms for average claims for outpatient (OP_AvgClaims) and inpatient (IP_AvgClaims) services.

### Data Pre-Processing

Data preprocessing involves:

- Mapping gender values and converting race data to categorical variables.
- Converting date columns to DateTime format.
- Creating a boolean column 'dead' to identify deceased beneficiaries.
- Calculating age and converting location data to categorical variables.
- Handling null values and creating boolean columns for renal disease indicator and coverage duration.

### Feature Engineering

Feature engineering includes:

- Aggregating features, merging data frames, and preparing data for model training.
- Renaming columns, dropping unnecessary index columns, and merging datasets with training labels.

## Machine Learning Models

The project uses three machine learning models to detect fraudulent providers:

1. **Logistic Regression**
2. **Random Forest**
3. **XGBoost**

## Results

### Logistic Regression

- Training accuracy: 78.32%
- Test accuracy: 79.86%
- ROC score: 0.91
- Higher recall for class 1 (0.90) but lower precision (0.29)

### Random Forest

- Training accuracy: 100%
- Test accuracy: 94.22%
- ROC score: 0.96
- Balanced precision (0.80) and recall (0.45) for class 1

### XGBoost

- Training accuracy: 98.18%
- Test accuracy: 93.62%
- ROC score: 0.95
- Balanced precision (0.69) and recall (0.49) for class 1

## Conclusion

The Random Forest model demonstrated the highest test accuracy and ROC score, indicating superior performance in detecting fraudulent medical providers. XGBoost also performed well, showing competitive results. Logistic Regression showed moderate performance, particularly in recall for positive cases.

## Authors

- Raja Muppidi


## Acknowledgments

- Data sourced from [Kaggle](https://www.kaggle.com/)
