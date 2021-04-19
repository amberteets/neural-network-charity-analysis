# Neural Network Charity Analysis

## Background & Purpose

Design a binary classifier capable of predicting whether applicants for philanthropic donations will be successful if funded.

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

    The deep learning model structure is as follows:
    
    <kdb> <img src="https://github.com/amberteets/neural-network-charity-analysis/blob/main/Resources/model_structure.png" /> </kbd>
    
    - The first hidden layer uses 132 neurons and the Sigmoid activation function.
    - The second hidden layer uses 88 neurons and the ReLU activation function.
    - The third hidden layer uses 44 neurons and the Sigmoid activation function.
    - The fourth hidden layer uses 10 neurons and the Sigmoid activation function.
    - The output layer uses the Sigmoid activation function.

  The number of hidden layers was determined via trial and error, while the number of neurons for each layer is based on the principle that there should be approximately two to three times the number of neurons per hidden layer as the number of input dimensions. The Sigmoid and ReLU activation functions were utilized due to their efficacy when dealing with positive nonlinear input data and binary classification.

  - Target Model Performance

    Target model performance of 75% accuracy was not achieved.

  - Optimization Strategy

    To try and increase model performance, a testing function was created to enable easy modification of model parameters such as the number of hidden layers, number of neurons, and types of activation functions used. Through trial-and-error, parameters were optimized to maximize model accuracy.
    
    Supplementary data preprocessing was also employed to attempt to improve model accuracy. An extra feature, the natural log of `ASK_AMT`, was added to mitigate model confusion caused by large range of `ASK_AMT` values.

## Summary

The deep learning model is approximately 72.7% accurate. A supervised learning model such as a support vector machine or random forest may have been more effective in solving this classification problem. In particular, because random forest models are less susceptible to influence from outliers, this model may produce a higher accuracy than the deep learning model.
