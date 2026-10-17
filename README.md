# Titanic Survival Prediction

A binary classification project that predicts passenger survival on the Titanic using logistic regression implemented from scratch with NumPy and Pandas.

## Overview

The objective is to predict whether a passenger survived the Titanic disaster based on passenger attributes. The model is implemented without using machine-learning libraries such as scikit-learn, providing a practical implementation of the mathematics behind logistic regression.

## Dataset

The project uses the Titanic passenger dataset, containing information such as:

- Passenger class (`Pclass`)
- Sex
- Age
- Number of siblings and spouses aboard (`SibSp`)
- Number of parents and children aboard (`Parch`)
- Fare
- Port of embarkation (`Embarked`)

The target variable is `Survived`, where `0` represents did not survive and `1` represents survived.

## Methodology

### 1. Data preprocessing

- Handled missing `Age` values using the training-set median.
- Handled missing `Embarked` values using the training-set mode.
- Converted categorical variables into numerical features using one-hot encoding.
- Standardized numerical features using statistics calculated from the training set.
- Split the data into training, validation, and test sets.

### 2. Logistic regression from scratch

Implemented logistic regression using NumPy, including:

- Sigmoid activation function
- Binary cross-entropy loss
- Gradient descent optimization
- L2 regularization
- Prediction using a probability threshold of 0.5

The model parameters are optimized by minimizing binary cross-entropy using gradient descent.

### 3. Model selection

Compared different learning rates and L2 regularization strengths. Selected the regularization parameter using validation binary cross-entropy, keeping the test set separate for final evaluation.

### 4. Evaluation

Evaluated the selected model using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Binary cross-entropy loss

## Results

Final test-set metrics are reported in the notebook. They should be updated here after the final version of the notebook has been executed.

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## Project Structure

```text
Titanic-Survival-Prediction/
├── titanic_survivers.ipynb
├── titanic.csv
└── README.md
```

## How to Run

1. Clone the repository.
2. Install the required dependencies.
3. Open the notebook in Jupyter Notebook or VS Code.
4. Run the cells from top to bottom.

Install the dependencies with:

```bash
pip install numpy pandas matplotlib jupyter
```

Ensure `titanic.csv` is in the same directory as the notebook.

## Key Learning Outcomes

- Implementing logistic regression without a machine-learning framework
- Understanding gradient descent and binary cross-entropy
- Applying data preprocessing without data leakage
- Using L2 regularization and validation-based model selection
- Evaluating binary classification models using multiple metrics
