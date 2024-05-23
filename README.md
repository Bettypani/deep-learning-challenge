# Alphabet Soup Nonprofit Foundation Funding Analysis

## Overview of the Analysis

The purpose of this analysis is to develop a tool that can help the nonprofit foundation Alphabet Soup select applicants for funding who have the best chance of success in their ventures. By analyzing historical data, the goal is to build a predictive model to determine the likelihood of a project's success based on various characteristics.

## Results

### Data Preprocessing

**Target Variable:**
- `IS_SUCCESSFUL`: This column indicates whether the project was successful. It is the target variable for our model, as we aim to predict the success of projects.

**Feature Variables:**
- `APPLICATION_TYPE`: Alphabet Soup application type
- `AFFILIATION`: Affiliated sector of industry
- `CLASSIFICATION`: Government organization classification
- `USE_CASE`: Use case for funding
- `ORGANIZATION`: Organization type
- `STATUS`: Active status
- `INCOME_AMT`: Income classification
- `ASK_AMT`: Funding amount requested

**Variables to Remove:**
- `NAME`: Not relevant for prediction
- `EIN`: Employer Identification Number, not relevant for prediction

### Compiling, Training, and Evaluating the Model

**Model Architecture:**
- **Input Layer:** Features from the dataset
- **Hidden Layers:** 
  - Three hidden layers
  - Each with 90 neurons
  - Activation function: ReLU (Rectified Linear Unit)
- **Output Layer:**
  - Single neuron
  - Activation function: Sigmoid (for binary classification)

**Model Performance:**
- **Target Performance:** The model's performance did not significantly improve even after adding a third hidden layer with 90 neurons and removing the `SPECIAL_ACCOMMODATION` column.
- **Achieved Accuracy:** 72.8%

**Steps Taken to Improve Performance:**
- Added a third hidden layer
- Adjusted the number of neurons in all layers
- Experimented with removing different columns and ultimately removed the `SPECIAL_ACCOMMODATION` column

### Summary

The deep learning model achieved an accuracy of 72.8%. Despite efforts to enhance performance by adding more hidden layers and tuning the number of neurons, the model did not show substantial improvement.

**Recommendation:**
To potentially achieve better performance, it is recommended to explore different machine learning models. A Random Forest classifier machine might provide better results for this classification problem. These models can handle the complexity of the data more effectively and often perform well on structured data.
