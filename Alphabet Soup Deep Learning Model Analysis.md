# Alphabet Soup Deep Learning Model Analysis

The purpose of this analysis was to build a deep learning model to predict whether a charity organization funded by Alphabet Soup would be successful based on the data that was provided. By utilizing historical data on charity applications, the objective was to develop a model that could identify key factors contributing to a successful funding outcome.

---

## Results

### Data Preprocessing
- **Target Variable**:
  - The target variable for the model was **`IS_SUCCESSFUL`**, which indicates whether a charity’s application was successful = 1 or not = 0.
  
- **Feature Variables**:
  - The features used in the model included:
    - `APPLICATION_TYPE`
    - `AFFILIATION`
    - `CLASSIFICATION`
    - `USE_CASE`
    - `ORGANIZATION`
    - `STATUS`
    - `INCOME_AMT`
    - `SPECIAL_CONSIDERATIONS`
    - `ASK_AMT`
  
- **Removed Variables**:
  - I removed columns from the dataset as they were not relevant for predicting success:
    - **`EIN`**: A unique identifier to each organization but not useful for prediction.
    - **`NAME`**: The name of the organization does not affect the success of funding.

### Compiling, Training, and Evaluating the Model
- **Model Architecture**:
  - **Number of Layers and Neurons**:
    - The model included:
      - **Input Layer**: 80 neurons, using `ReLU` activation.
      - **First Hidden Layer**: 80 neurons, using `ReLU` activation.
      - **Second Hidden Layer**: 30 neurons, using `ReLU` activation.
      - **Output Layer**: 1 neuron with `sigmoid` activation for binary classification.
  - **Activation Functions**:
    - The `ReLU` activation function was used for the hidden layers because it helps with faster training and reduces the likelihood of vanishing gradients.
    - The `sigmoid` activation function was used in the output layer to produce a probability between 0 and 1, suitable for binary classification.

- **Model Performance**:
  - The model was trained with **50 epochs** and a batch size of **32**.
  - **Achieved Accuracy**: The model reached an accuracy of approximately **72.65%** on the test data, which is slightly below the target performance of 75%.
  - **Loss**: The model’s final loss value was **0.5722**.

- **Steps Taken to Improve Performance**:
  -Several steps were taken to imporve performance:
    - Adding additional layers and increasing the number of neurons.
    - Adjusted the number of epochs and batch sizes.
    - Implemented dropout layers to prevent overfitting.

---

## Summary
- **Overall Results**:
  - The neural network model achieved an accuracy of **72.65%**, which fell short of the desired performance target of 75%. The model demonstrated a moderate ability to predict the success of charity applications but may require further optimization or adjustments to improve its predictive power.
