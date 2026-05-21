# Titanic Survival Prediction

A beginner-friendly machine learning project that predicts whether a passenger survived the Titanic disaster using Logistic Regression.

## Problem Statement
The aim of this project is to build a classification model that predicts passenger survival on the Titanic using available passenger details. This is a binary classification problem where the target is whether a passenger survived or not.

## Dataset
This project uses the `Titanic-Dataset.csv` dataset.

Main columns available in the dataset include:
- `PassengerId`
- `Survived`
- `Pclass`
- `Name`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Ticket`
- `Fare`
- `Cabin`
- `Embarked`

Target column:
- `Survived`

Final feature columns used in the model:
- `Pclass`
- `Sex`
- `Age`
- `Fare`

## Steps Performed
1. Imported required Python libraries.
2. Loaded the Titanic dataset using pandas.
3. Inspected the dataset using `head()` and null-value checks.
4. Cleaned the data:
   - Filled missing `Age` values with the mean age.
   - Filled missing `Embarked` values with the most frequent value.
   - Dropped the `Cabin` column due to too many missing values.
5. Performed exploratory data analysis (EDA):
   - Count plot of survival
   - Survival by sex
   - Family size distribution
6. Created a new feature:
   - `FamilySize = SibSp + Parch`
7. Converted categorical columns into numeric values:
   - `Sex`: male = 0, female = 1
   - `Embarked`: S = 0, C = 1, Q = 2
8. Selected the input features and target variable.
9. Split the data into training and testing sets.
10. Trained a Logistic Regression model.
11. Predicted survival on the test set.
12. Evaluated the model using accuracy score.

## Models Used
### Logistic Regression
The notebook uses a Logistic Regression classifier with:
- `max_iter=1000`

## Results (Accuracy)
Accuracy obtained in the notebook:
- **0.7877094972067039**

Rounded accuracy:
- **78.77%**

## Conclusion
This project shows a complete beginner-level machine learning workflow on the Titanic dataset.

Key learnings:
- Data cleaning is important before training a model.
- Even a simple model like Logistic Regression can provide solid baseline performance.
- Passenger class, sex, age, and fare are useful features for predicting survival.

## Project Structure
```text
titanic_model/
├── .gitignore
├── README.md
├── requirements.txt
└── titanic_model.ipynb
```

## How to Run
1. Place `Titanic-Dataset.csv` in the same folder as the notebook.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `titanic_model.ipynb` in Jupyter Notebook or VS Code.
4. Run the notebook cells in order.

## GitHub Repository Description
Titanic survival prediction project using Logistic Regression, data preprocessing, feature selection, and exploratory data analysis in Python.
