# Healthcare Data Preprocessing & Outlier Treatment

## Overview

This project focuses on data preprocessing, missing value imputation, and outlier treatment on a healthcare dataset. The objective is to transform raw patient health data into a clean, structured, and machine learning-ready dataset.

The dataset simulates real-world healthcare records containing inconsistencies such as missing values and extreme outliers due to measurement errors. This project demonstrates how to handle such issues using multiple statistical and machine learning techniques.

---

## Objective

- Identify and analyze missing values in the dataset
- Apply multiple imputation techniques and compare results
- Detect and handle outliers using statistical methods
- Improve overall data quality and usability
- Prepare dataset for machine learning applications (Disease Risk Prediction)

---

## Problem Statement

You are working as a Data Analyst in a healthcare domain, where patient data contains missing entries and extreme values. Your task is to clean and preprocess the dataset so that it becomes suitable for predictive modeling (e.g., disease risk classification).

---

## Dataset Description

The dataset contains patient health records with the following features:

| Feature | Description |
|---|---|
| `patient_id` | Unique identifier for each patient |
| `age` | Age of the patient |
| `gender` | Male / Female |
| `region` | Geographic region |
| `bmi` | Body Mass Index |
| `blood_pressure` | Blood pressure level |
| `cholesterol` | Cholesterol level |
| `glucose` | Glucose level |
| `disease_risk` | Target variable (0 = Low, 1 = High) |

---

## Part A: Handling Missing Values

### Missing Value Analysis

- Calculated percentage of missing values per column
- Identified columns requiring imputation

### Imputation Techniques Applied

**Simple Imputer (Mean & Median)**
Used for numerical features like BMI, Age, Cholesterol, and Glucose.

**Simple Imputer (Categorical)**
Missing values in the Region column replaced with the most frequent value.

**Most Frequent Imputation**
Applied on the Gender column.

**Missing Indicator + Random Sample Imputation**
Created binary indicator columns and filled missing values using random sampling from existing data.

**KNN Imputer**
Used nearest neighbors to estimate missing values.

**MICE (Iterative Imputer)**
Advanced multivariate imputation using chained equations.

---

## Part B: Handling Outliers

### Outlier Detection & Treatment Methods

**Z-score Method**
Identified extreme values based on standard deviation.

**IQR (Interquartile Range) Method**
Removed values outside the acceptable interquartile range.

**Percentile Method**
Capped values below the 1st percentile and above the 99th percentile.

**Winsorization**
Limited extreme values without removing data points.

### Comparison of Methods

| Method | Effect on Dataset Size | Notes |
|---|---|---|
| Z-score | Reduced | Removes outliers |
| IQR | Reduced | Removes outliers |
| Percentile | Preserved | Caps values |
| Winsorization | Preserved | Caps values |
| KNN Imputer | Preserved | More accurate imputation |
| MICE | Preserved | More accurate imputation |

---

## Visualization

- Boxplots used to visualize outliers before and after treatment
- Statistical summaries used to validate preprocessing steps

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- SciPy
- Matplotlib

---

## How to Run the Project

1. Download or clone this repository
2. Open the notebook: `healthcare.ipynb`
3. Run all cells sequentially

---

## Key Learnings

- Real-world datasets require extensive preprocessing
- Different imputation techniques yield different results
- Outlier handling is critical for model performance
- Advanced methods like KNN and MICE improve data quality

---

## Expected Outcome

After preprocessing:

- Missing values are handled effectively
- Outliers are treated using appropriate techniques
- Dataset is clean and ready for machine learning models

---

## Future Improvements

- Apply classification models (Logistic Regression, Random Forest)
- Evaluate model performance
- Deploy solution using Flask or Streamlit

---

## Author

Arnob Maity
