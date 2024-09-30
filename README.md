# Titanic - Machine Learning from Disaster 🚢

This project aims to solve the classic Titanic survival prediction problem from the [Kaggle Titanic competition](https://www.kaggle.com/c/titanic), using a machine learning model to predict whether a passenger survived or not based on certain features like age, gender, class, etc.

## Project Overview

The **Titanic competition** is a beginner-friendly Kaggle challenge where you build a predictive model to answer the question: **"Who will survive the Titanic disaster?"**

### Objective
The goal of this project is to:
- Build a machine learning model to predict the survival of passengers.
- Apply various techniques to avoid overfitting.
- Use models like **Gradient Boosting** to make accurate predictions.

## Dataset

- **Training Dataset**: `train.csv` - This file contains labeled data of passengers and their survival outcome.
- **Test Dataset**: `test.csv` - This file contains only passenger data, without survival outcome.
- **Submission File**: The submission file must include the `PassengerId` and `Survived` columns.

### Features

- `PassengerId`: ID of each passenger
- `Pclass`: Ticket class (1st, 2nd, 3rd)
- `Sex`: Gender of the passenger
- `Age`: Age of the passenger
- `SibSp`: Number of siblings/spouses aboard the Titanic
- `Parch`: Number of parents/children aboard the Titanic
- `Fare`: Passenger fare
- `Embarked`: Port of Embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)

## Installation and Setup

1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/titanic-prediction.git
    ```

2. Navigate to the project directory:
    ```bash
    cd titanic-prediction
    ```

3. Download the dataset:
    - Download the `train.csv` and `test.csv` files from [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic/data).
    - Place them in the `data/` directory.

4. Run the notebook or Python script to train the model and generate predictions:
    ```bash
    jupyter notebook OPTIMIZED.ipynb
    ```

## Model Overview

We use the **Gradient Boosting Classifier** as our main model due to its performance on the training data. The model is trained with various preprocessing steps to ensure it generalizes well on unseen data.

### Key Steps:
1. **Data Preprocessing**: 
   - Handle missing values in `Age`, `Embarked`, and `Fare`.
   - Convert categorical variables like `Sex` and `Embarked` into numerical representations.
   - Feature scaling using `StandardScaler`.

2. **Model Training**:
   - Model: **Gradient Boosting Classifier**
   - Parameters: Tuned using cross-validation to avoid overfitting.

3. **Prediction and Submission**:
   - After training, predictions are made on the test data.
   - A CSV file is generated for submission to Kaggle.

## Submission

The final predictions are saved in `titanic_submission.csv` for upload to the Kaggle competition. The submission file contains two columns:
- `PassengerId`: The ID of the passenger.
- `Survived`: The predicted survival status (0 = Did not survive, 1 = Survived).

## Results

The model's performance is evaluated based on the accuracy of predictions in comparison to the ground truth data. Our final leaderboard score on Kaggle is **[Insert Score Here]**.

## Repository Structure

```plaintext
├── data/
│   ├── train.csv          # Training data
│   ├── test.csv           # Test data
├── notebooks/
│   ├── titanic.ipynb    # Jupyter notebook for model training
├── titanic_submission.csv # Final submission file
├── README.md              # Project overview
