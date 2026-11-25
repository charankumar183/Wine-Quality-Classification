# Wine Quality Classification Using Machine Learning

## 1. Project Overview

This project uses supervised Machine Learning classification algorithms to predict wine quality based on its physicochemical properties.

The model analyzes chemical characteristics such as acidity, alcohol content, density, pH, and sulphates to classify wine into Good or Bad quality categories.

## 2. Problem Statement

Wine quality depends on various physicochemical properties. The objective of this project is to develop a Machine Learning classification model that predicts whether wine belongs to the Good or Bad quality category based on its chemical properties.

## 3. Dataset

- **Source:** Kaggle
- **Dataset:** Wine Quality Dataset (WineQT)
- **Total Records:** 1,143
- **Total Columns:** 13 (including ID and target)
- **Input Features:** 11 physicochemical properties
- **Target Variable:** Quality

**Dataset Link:** https://www.kaggle.com/datasets/yasserh/wine-quality-dataset

### Input Features

1. Fixed Acidity
2. Volatile Acidity
3. Citric Acid
4. Residual Sugar
5. Chlorides
6. Free Sulfur Dioxide
7. Total Sulfur Dioxide
8. Density
9. pH
10. Sulphates
11. Alcohol

## 4. Technologies and Libraries Used

- Python
- Pandas – Data manipulation and analysis
- NumPy – Numerical operations
- Matplotlib – Data visualization
- Seaborn – Statistical visualization
- Scikit-learn – Machine Learning model development and evaluation
- Joblib – Model serialization and saving

## 5. Machine Learning Algorithms

Two supervised classification algorithms were implemented:

### 1. Logistic Regression
Used as a baseline classification algorithm to predict wine quality categories.

### 2. Random Forest Classifier
Used an ensemble of decision trees to classify wine quality and compare its performance with Logistic Regression.

## 6. Project Workflow

1. Dataset collection from Kaggle.
2. Data loading using Pandas.
3. Data exploration and understanding.
4. Missing value and duplicate checking.
5. Data cleaning and preprocessing.
6. Removal of unnecessary ID column.
7. Exploratory Data Analysis (EDA).
8. Conversion of wine quality scores into binary categories.
9. Feature selection.
10. Train-test splitting (80% training and 20% testing).
11. Feature scaling using StandardScaler for Logistic Regression.
12. Model training using Logistic Regression.
13. Model training using Random Forest.
14. Model evaluation and comparison.
15. Prediction on new wine samples.
16. Saving the trained model using Joblib.

## 7. Classification Categories

The original wine quality scores were converted into two categories:

| Quality Score | Category | Label |
|---|---|---|
| Below 7 | Bad Quality | 0 |
| 7 or Above | Good Quality | 1 |

This converts the original quality prediction problem into a binary classification problem.

## 8. Model Evaluation

The models were evaluated using the following performance metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Model Performance Comparison

| Algorithm | Accuracy |
|---|---:|
| Logistic Regression | 86.46% |
| Random Forest Classifier | 92.14% |

**Best Performing Model:** Random Forest Classifier

Random Forest achieved 92.14% accuracy, outperforming Logistic Regression on the test dataset.

## 9. Prediction

The trained model was tested using a new wine sample containing physicochemical properties.

The model predicted:

**Predicted Wine Quality: Bad**

The trained model was saved and loaded using Joblib to perform predictions without retraining.

## 10. Model Saving

The trained machine learning model and associated preprocessing information were saved using Joblib.

**Saved Model:** `wine_quality_model.pkl`

This allows the trained model to be reused for future predictions.

## 11. Conclusion

Successfully developed a supervised Machine Learning classification project to predict wine quality based on physicochemical properties.

Implemented and compared Logistic Regression and Random Forest classification algorithms. Random Forest achieved 92.14% accuracy and performed better than Logistic Regression on the test dataset.

This project provided practical experience in data preprocessing, exploratory data analysis, feature selection, classification model development, model evaluation, and model saving.

## 12. Project Structure

```text
Wine-Quality-Classification/
│
├── dataset/
│   └── WineQT.csv
│
├── wine_quality.ipynb
├── wine_quality_model.pkl
├── README.md
└── .gitignore
```

## 13. How to Run the Project

1. Clone or download the repository.
2. Install the required Python libraries.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

3. Open the project in VS Code.
4. Open `wine_quality.ipynb`.
5. Select the Python environment.
6. Execute the notebook cells sequentially to run the complete workflow.