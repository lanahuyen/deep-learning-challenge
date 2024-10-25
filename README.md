# Alphabet Soup Charity - Deep Learning Model Report

## Overview of the Analysis

The goal of this analysis was to build a machine learning model that can predict whether organizations funded by Alphabet Soup will be successful. Using data from past funding decisions, we created a binary classifier to help Alphabet Soup make better decisions when choosing who to fund.

## Results

### Data Preprocessing

- **Target Variable**: The target for this model is the `IS_SUCCESSFUL` column, which tells us if the organization was successful or not.
- **Feature Variables**: The features used in the model include:
  - `APPLICATION_TYPE`: The type of application submitted.
  - `AFFILIATION`: The sector or industry the organization is affiliated with.
  - `CLASSIFICATION`: The government classification of the organization.
  - `USE_CASE`: The reason for funding.
  - `ORGANIZATION`: The type of organization.
  - `STATUS`: Whether the organization is still active.
  - `INCOME_AMT`: The income category of the organization.
  - `SPECIAL_CONSIDERATIONS`: Whether there were any special conditions for the application.
  - `ASK_AMT`: The amount of money requested.
- **Removed Variables**: The `EIN` and `NAME` columns were removed because they were just identifiers and didn’t add value to the model.

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions**:
  - The model used 2 hidden layers:
    - The first layer had 100 neurons and used the ReLU activation function.
    - The second layer had 50 neurons and also used ReLU.
  - The output layer had 1 neuron with a sigmoid activation function, which is used for binary classification.
- **Model Performance**: 
  - The model didn’t hit the target accuracy of 75%. After trying different settings, the best accuracy we got was around **73%-74%**.
- **Optimization Attempts**:
  - We tried several different settings, like adding and removing neurons in the hidden layers.
  - A third hidden layer was tested, as well as different activation functions (like LeakyReLU).
  - Dropout layers were added to prevent overfitting, but that didn’t improve the accuracy enough.
  - We also tried changing the learning rate and increasing the number of training epochs.

### Summary

Overall, we trained and tested the deep learning model with various adjustments, but the best accuracy we could achieve was around **74%**. While this is a good result, it didn’t meet the target of 75%.

#### Recommendation:

To improve results, we could try other machine learning models that work better with this type of data, like **XGBoost** or **Random Forests**. These models are often better for structured, tabular data like this and might give us better accuracy. We could also try more advanced feature engineering to create new features from the data.
