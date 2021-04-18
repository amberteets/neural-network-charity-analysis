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

    Target model performance of 75% accuracy was not achieved.

  - Optimization Strategy

    To try and increase model performance, a testing function was created to enable easy modification of model parameters such as the number of hidden layers, number of neurons, and types of activation functions used. Through trial-and-error, parameters were optimized to maximize model accuracy.
    
    Supplementary data preprocessing was also employed to attempt to improve model accuracy. An extra feature, the natural log of `ASK_AMT`, was added to mitigate model confusion caused by large range of `ASK_AMT` values.

## Summary

The deep learning model is approximately ... accurate. 
