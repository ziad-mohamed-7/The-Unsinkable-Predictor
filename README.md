# The Unsinkable Predictor

## Project Overview
The **Unsinkable Predictor** is a machine learning project focused on predicting passenger survival on the Titanic. The project involves data cleaning, preprocessing, exploratory data analysis (EDA), and training machine learning models to achieve optimal predictions.

## Dataset
The project uses Titanic datasets:
- `train.csv` for training and validation.
- `test.csv` for final predictions.

## Features
The dataset includes features such as:
- `Pclass`: Ticket class (1st, 2nd, 3rd).
- `Age`: Age of the passenger.
- `SibSp`: Number of siblings/spouses aboard.
- `Parch`: Number of parents/children aboard.
- `Fare`: Passenger fare.
- `Sex` and `Embarked`: Encoded as one-hot variables.

## Libraries Used
- `pandas` for data manipulation
- `matplotlib` and `seaborn` for visualization
- `scikit-learn` for machine learning models and metrics

## Steps in the Project

### 1. Data Cleaning and Preprocessing
- **Handling Missing Values**:
  - Filled `Age` and `Fare` with their respective medians.
  - Replaced missing `Embarked` values with the mode.
  - Dropped the `Cabin`, `Name`, and `Ticket` columns due to irrelevance or high missing rates.

- **Feature Encoding**:
  - Applied one-hot encoding to `Sex` and `Embarked`.

- **Feature Selection**:
  - Selected key features for modeling: `Pclass`, `Age`, `SibSp`, `Parch`, `Fare`, `Sex_male`, `Embarked_Q`, `Embarked_S`.

### 2. Exploratory Data Analysis (EDA)
- Visualized correlations using a heatmap.
- Analyzed feature relationships with survival rates using plots.

### 3. Model Training
- **Logistic Regression**:
  - Trained on 80% of the training data.
  - Accuracy: 81.0%, Precision: 78.6%, F1 Score: 76.4%.

- **Decision Tree Classifier**:
  - Trained on the same data split.
  - Accuracy: 78.2%, Precision: 72.7%, F1 Score: 74.2%.

### 4. Model Evaluation
Models were evaluated on the validation set using metrics like:
- **Accuracy**: Proportion of correct predictions.
- **Precision**: Ratio of true positives to total predicted positives.
- **F1 Score**: Harmonic mean of precision and recall.

### 5. Prediction and Results
- Generated survival predictions for the test dataset using both models.
- Results were saved as CSV files:
  - `logistic_regression_results.csv`
  - `decision_tree_results.csv`

### 6. EDA on Test Predictions
Conducted further analysis on predicted test results, visualizing the relationships between features (e.g., `Age`, `Pclass`, `Fare`) and survival outcomes.

## File Structure
- `train.csv`: Training dataset.
- `test.csv`: Test dataset.
- `unsinkable_predictor.ipynb`: Main notebook for analysis and modeling.
- `logistic_regression_results.csv`: Predictions from Logistic Regression.
- `decision_tree_results.csv`: Predictions from Decision Tree Classifier.
