# Building a regression model to predict Graduate Admission Chances on behalf of Jamboree, based on student's features like performance in undergraduate, university, TOEFL, GRE, research etc

## Overview

This repository contains the analysis and development of a predictive model to estimate the chances of Indian students gaining admission to Ivy League graduate programs. The goal is to identify key factors influencing graduate admissions and predict the likelihood of admission based on student profiles. We used various regression techniques, including linear regression, polynomial regression, and regularization methods (Lasso and Ridge), to build an accurate predictive model.

The dataset provided by Jamboree includes important features such as GRE scores, TOEFL scores, undergraduate GPA, university ratings, strength of SOP/LOR, and research experience. The analysis and model developed in this project will help students understand their chances of admission and provide actionable insights to improve their profiles.

## Table of Contents

- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Modeling Techniques](#modeling-techniques)
  - [Linear Regression](#linear-regression)
  - [Polynomial Linear Regression](#polynomial-linear-regression)
  - [Regularization (Lasso, Ridge)](#regularization-lasso-ridge)
- [Model Evaluation](#model-evaluation)
- [Business Insights](#business-insights)
- [Conclusion](#conclusion)
- [Requirements](#requirements)
- [License](#license)

## Problem Statement

The goal of this case study is to predict the **Chance of Admit** (ranging from 0 to 1) based on various input features like GRE scores, TOEFL scores, university ratings, SOP/LOR strength, undergraduate GPA, and research experience. This will help students understand the factors that most influence their chances of admission to Ivy League colleges and how they can improve their profiles to increase their likelihood of acceptance.

## Dataset

The dataset used for this project is **jamboree_admission.csv** and contains the following columns:

- **Serial No.**: Unique identifier for each row.
- **GRE Scores**: Graduate Record Examination scores (out of 340).
- **TOEFL Scores**: Test of English as a Foreign Language scores (out of 120).
- **University Rating**: Rating of the university (out of 5).
- **SOP and LOR Strength**: Combined strength of the student's SOP and LOR (out of 5).
- **Undergraduate GPA**: Grade Point Average of the student's undergraduate degree (out of 10).
- **Research Experience**: Binary variable indicating whether the student has research experience (0 = No, 1 = Yes).
- **Chance of Admit**: Probability of the student being admitted to the graduate program (ranging from 0 to 1).

## Data Preprocessing

The data preprocessing steps include:

- Handling missing values (if any).
- Scaling numerical features to ensure consistency.
- Encoding categorical variables (Research Experience) for model compatibility.
- Splitting the data into training and testing sets.

## Exploratory Data Analysis (EDA)

In the EDA phase, we performed the following:

- Visualized the distribution of features and the target variable.
- Analyzed correlations between features and the target variable.
- Identified trends, outliers, and potential data quality issues.
- Examined relationships between various features to better understand their impact on the admission chances.

## Modeling Techniques

### Linear Regression

We began by building a **Linear Regression** model to predict the target variable, **Chance of Admit**, using the available features. This model serves as the baseline for comparison with more complex models.

### Polynomial Linear Regression

To capture potential non-linear relationships between features and the target, we extended the linear model to **Polynomial Linear Regression**. This model includes higher-degree terms to improve the prediction accuracy.

### Regularization (Lasso, Ridge)

To prevent overfitting and improve model generalization, we applied **Lasso** (L1 regularization) and **Ridge** (L2 regularization) techniques. These methods help control model complexity by penalizing large coefficients.

## Model Evaluation

We evaluated the performance of each model using the following metrics:

- **R-squared**: To measure the proportion of variance explained by the model.
- **Mean Squared Error (MSE)**: To evaluate the average squared difference between predicted and actual values.
- **Root Mean Squared Error (RMSE)**: To assess the model’s prediction accuracy.

We compared the results of all models and selected the one with the best performance in terms of minimizing error and maximizing explanatory power.

## Business Insights

From the analysis and modeling, we derived several actionable business insights:

1. **GRE and TOEFL Scores**: High GRE and TOEFL scores are critical for improving admission chances, but they should be complemented with other strong factors like research experience and SOP/LOR strength.
2. **Research Experience**: Students with research experience tend to have a higher chance of admission, especially to top-tier universities.
3. **Undergraduate GPA**: A higher undergraduate GPA is positively correlated with better chances of admission, but it should be backed by strong test scores and recommendations.
4. **SOP/LOR Strength**: A strong Statement of Purpose and Letters of Recommendation are essential for students aiming for Ivy League colleges, as they significantly impact admission chances.

## Conclusion

This project demonstrates how data-driven analysis can predict graduate admission chances and provide valuable insights for students. By understanding the key factors that influence admissions, students can strategically improve their profiles to increase their chances of success.

## Requirements

- Python 3.x
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-learn
