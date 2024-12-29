# 10-Year Heart Disease Risk Prediction

A machine learning project to predict the risk of developing heart disease within 10 years based on various health indicators and lifestyle factors.

## Overview

This project aims to predict whether a person will develop heart disease within 10 years using different machine learning models. The prediction is based on various factors, including patient background, behavioral data, medical history, and current clinical measurements.

## Dataset Description

### Background Data
- **Sex**: Gender of the patient (M/F)
- **Age**: Patient's age (Discrete number)
- **Education**: Education level (Categorical: 1-4)

### Behavioral Data
- **is_smoking**: Current smoking status (YES/NO)
- **CigsPerDay**: Average number of cigarettes smoked per day (Discrete number)

### Medical History
- **BPMeds**: Blood pressure medication status (0: NO, 1: YES)
- **Prevalent_Stroke**: Previous stroke history (0: NO, 1: YES)
- **Prevalent_Hyp**: Hypertension history (0: NO, 1: YES)
- **Diabetes**: Diabetes status (0: NO, 1: YES)

### Current Clinical Measurements
- **TotChol**: Total cholesterol level (mg/dL)
- **SysBP**: Systolic blood pressure (mmHg)
- **DiaBP**: Diastolic blood pressure (mmHg)
- **BMI**: Body Mass Index (kg/m²)
- **Heart_Rate**: Heart rate (bpm)
- **Glucose**: Blood glucose level (mg/dL)

### Target Variable
- **TenYearCHD**: 10-year risk of coronary heart disease (0: NO, 1: YES)

## Models Implemented

### 1. K-Nearest Neighbors (KNN)
- Initial implementation with basic preprocessing
- Enhanced implementation with correlation coefficient weighting
- **Best accuracy achieved**: 86% (with weighting)  
- **F1-score**: 0.06 (with weighting)

### 2. Naive Bayes
#### Gaussian NB
- **Accuracy**: 82%  
- **F1-score**: 0.24  
#### Bernoulli NB
- **Accuracy**: 82%  
- **F1-score**: 0.23  

### 3. Decision Tree
- **Accuracy**: 85%  
- **F1-score**: 0.06  

## Data Preprocessing Techniques

### Missing Value Treatment
- **Numerical features**: Mean imputation
- **Categorical features**: Mode imputation

### Feature Normalization
- **Z-score normalization** for continuous variables
- **Min-max normalization** for specific features

### Categorical Encoding
- Binary encoding for yes/no features
- Numeric encoding for categorical variables

### Feature Engineering
- Correlation-based feature weighting
- Clinical threshold-based discretization

## Key Findings
- Feature weighting based on correlation coefficients improved KNN model performance.
- Continuous clinical measurements performed better without discretization.
- Naive Bayes models showed balanced precision and recall scores.
- Decision Tree and weighted KNN achieved similar accuracy levels.
- Most models showed high precision but lower recall scores.

## Performance Comparison

| Model                 | Accuracy | F1-Score |
|-----------------------|----------|----------|
| KNN (Basic)           | 0.84     | 0.03     |
| KNN (Weighted)        | 0.86     | 0.06     |
| Naive Bayes (Gaussian)| 0.82     | 0.24     |
| Naive Bayes (Bernoulli)| 0.82    | 0.23     |
| Decision Tree         | 0.85     | 0.06     |

## Technologies Used
- **Python**
- **Scikit-learn**
- **Pandas**
- **NumPy**
- **Matplotlib/Seaborn** for visualizations
