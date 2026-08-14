# Titanic Survival Prediction

## About the Titanic

The sinking of the Titanic is one of the most well-known maritime disasters in history.

On April 15, 1912, during her maiden voyage, the RMS Titanic sank after colliding with an iceberg. There were not enough lifeboats for everyone on board, and approximately 1,500 people lost their lives.

This project uses the well-known **Titanic dataset** to explore the factors associated with passenger survival and to develop and compare different **binary classification models**.

The project is inspired by the [Titanic competition on Kaggle](https://www.kaggle.com/c/titanic). However, the objective of this project is **not to compete in the Kaggle challenge**, but rather to use the dataset as a practical case study for learning and experimenting with machine learning classification techniques.

## Project Objectives

The main objectives of this project are:

* Explore and perform descriptive analysis of the Titanic dataset.
* Identify variables that may be relevant for predicting passenger survival.
* Perform data preprocessing and handle missing values.
* Transform categorical variables into dummy variables.
* Analyze correlations between features and identify potentially redundant variables.
* Compare different binary classification algorithms.
* Evaluate model performance using Accuracy, F1-Score, and ROC AUC.
* Select a promising model for further optimization.
* Perform hyperparameter tuning using cross-validation.
* Generate predictions for the Kaggle test dataset.

## Data Preprocessing

The dataset contains several passenger characteristics, including:

* Passenger class (`Pclass`)
* Sex (`Sex`)
* Age (`Age`)
* Number of siblings and spouses aboard (`SibSp`)
* Fare (`Fare`)
* Port of embarkation (`Embarked`)
* Passenger title (`Title`)

During the preprocessing stage, missing values were investigated and treated according to the characteristics of each variable.

For example, missing `Age` values were imputed using the mean age of passengers within the corresponding passenger class. Missing `Fare` values were handled using the mean fare for third-class passengers, while missing `Embarked` values were replaced with the most frequent embarkation port.

The `Title` variable was also simplified by retaining the most frequent titles (`Mr`, `Miss`, `Mrs`, and `Master`) and grouping less frequent titles into a single `Person` category.

Variables such as `Ticket` and `Cabin` were excluded from the final model because they were considered unsuitable for the modeling approach used in this project.

## Classification Models

Several classification algorithms were evaluated:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)
* Random Forest
* Gradient Boosting
* XGBoost
* Multilayer Perceptron (MLP)

The models were evaluated using cross-validation on the training data.

The main evaluation metrics were:

* **Accuracy** — proportion of correctly classified observations.
* **F1-Score** — harmonic mean of precision and recall.
* **ROC AUC** — measures the model's ability to discriminate between the two classes across different classification thresholds.

## Model Selection

Among the models evaluated, **Gradient Boosting and XGBoost achieved the strongest overall performance**.

Gradient Boosting obtained the highest Accuracy and ROC AUC, while XGBoost achieved the highest F1-Score. Since the differences between the two models were relatively small, XGBoost was selected for further development based on its competitive predictive performance, its higher F1-Score, and its flexibility for hyperparameter optimization.

XGBoost also provides useful features for controlling model complexity and overfitting, as well as computational optimizations and support for parallel processing.

## Hyperparameter Tuning

After selecting XGBoost, a grid search with 10-fold cross-validation was used to evaluate different combinations of:

* `learning_rate`
* `max_depth`
* `n_estimators`

The purpose of this stage was to identify a combination of hyperparameters capable of improving the model's predictive performance.

## Project Structure

The project is organized into notebooks and data files covering the main stages of the analysis:

```text
titanic_project/
│
├── data/
│   ├── gender_submission.csv
│   ├── kaggle.csv
│   ├── train.csv
│   ├── test.csv
│   ├── titanic_train.csv
│   └── titanic_test.csv
│
├── notebooks/
│   ├── descriptive_analysis
│   └── model
│
└── README.md
```


## Technologies and Libraries

The project was developed in Python using common data science and machine learning libraries, including:

* Python
* pandas
* NumPy
* Matplotlib
* scikit-learn
* XGBoost
* Jupyter Notebook


The required libraries can be installed using `pip` or another Python environment/package management solution.

For example:

```bash
pip install pandas numpy matplotlib scikit-learn xgboost jupyter
```

## Kaggle Submission

Although participation in the Kaggle competition is not the primary objective of this project, the final stage generates a DataFrame containing `PassengerId` and the predicted `Survived` values in the format required for a Kaggle submission.

This step is included as an additional practical exercise in generating predictions from a trained classification model and preparing the output for an external evaluation platform.

## Purpose of the Project

This project is primarily a **machine learning learning exercise**. The Titanic dataset was chosen because it provides a well-known and relatively accessible binary classification problem while still allowing experimentation with important concepts such as:

* Exploratory data analysis
* Missing value treatment
* Feature engineering
* Categorical variable encoding
* Feature selection
* Correlation analysis
* Cross-validation
* Model comparison
* Evaluation metrics
* Hyperparameter tuning
* Ensemble learning
* Model prediction

The emphasis is therefore on understanding and applying the machine learning workflow rather than achieving a specific Kaggle ranking.
