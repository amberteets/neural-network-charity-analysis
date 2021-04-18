# Neural Network Charity Analysis

## Background & Purpose

Design a binary classifier capable of predicting whether applications for philanthropic donations will be successful if funded.

## Results

- **Data Preprocessing**

  - Target Variable
  
    The target variable for the model is `IS_SUCCESSFUL`, indicating whether or not past applications were successful if funded. The binary classifier will attempt to predict whether or not future applicants will be successful if funded.
  
  - Features

    Features include `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`. The binary classifier will use these characteristics to drive its predictions.

  - Extraneaous Variables

    Variables `EIN` AND `NAME` are simply identification columns (carry no predictive weight), and should be removed from input data.

- **Compiling, Training, and Evaluating the Model**

  - Neurons, Layers, and Activation Functions
  - Target Model Performance
  - Optimization Strategy

## Summary
