# Titanic Survival Prediction

A beginner data science capstone project that explores Titanic passenger data and uses Logistic Regression to predict passenger survival.

## Problem Statement

The goal of this project is to predict whether a Titanic passenger survived based on information such as their passenger class and sex.

Understanding which passenger characteristics were associated with survival provides an opportunity to apply data cleaning, exploratory data analysis, visualization, and machine learning techniques to a real-world dataset.

## Dataset

The dataset contains **891 passenger records** from the Titanic.

**Dataset source:** [Titanic Dataset](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)

### Key Columns

Some of the key columns used in the analysis include:

* `Survived` — whether the passenger survived
* `Pclass` — passenger class
* `Sex` — passenger sex
* `Age` — passenger age
* `SibSp` — number of siblings/spouses aboard
* `Parch` — number of parents/children aboard
* `Fare` — passenger fare
* `Embarked` — port of embarkation

The `Cabin`, `Name`, and `Ticket` columns were dropped during the analysis.

## My Approach

### 1. Data Cleaning

I first examined the dataset for missing values.

* Missing values in the `Age` column were filled using the **median**.
* Missing values in the `Embarked` column were filled using the **mode**.
* The `Cabin` column was dropped because it contained **687 missing values**, making it unsuitable for the analysis.
* The `Name` and `Ticket` columns were also dropped.

### 2. Exploratory Data Analysis

I explored the dataset to understand the distribution of survivors and identify relationships between passenger characteristics and survival.

The analysis showed that:

* **549 passengers did not survive.**
* **342 passengers survived.**
* More females survived than males.
* First-class passengers had the highest survival, while third-class passengers had the lowest.

### 3. Visualization

I created charts to help understand the patterns in the data.

One of the key visualizations was a **bar chart comparing survival by passenger class**, which showed that first-class passengers survived at a much higher rate than third-class passengers.

### 4. Modeling

I trained a **Logistic Regression** model because the target variable, `Survived`, represents a binary outcome: survived or did not survive.

## Key Findings

The analysis revealed several important patterns in the Titanic passenger data:

* Out of 891 passengers, **342 survived while 549 did not survive**.
* **More females survived than males**, which was one of the most interesting findings from the exploration.
* **First-class passengers survived the most**, while **third-class passengers survived the least**.
* Passenger class and sex were important areas of focus in understanding survival patterns.

## Model Results

The Logistic Regression model achieved an accuracy of **80.45%** on the test dataset.

This means the model correctly classified approximately **four out of every five passengers** in the test dataset.

### Confusion Matrix

The confusion matrix produced the following results:

* **98 True Negatives:** Passengers who did not survive and were correctly predicted not to survive.
* **46 True Positives:** Passengers who survived and were correctly predicted to survive.
* **12 False Positives:** Passengers predicted to survive who did not actually survive.
* **23 False Negatives:** Passengers predicted not to survive who actually survived.

Overall, the model achieved a reasonable level of predictive accuracy for this beginner machine learning project.

## Tools and Technologies

* **Python**
* **Pandas** — data manipulation and analysis
* **NumPy** — numerical operations
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization
* **scikit-learn** — machine learning and model evaluation

## How to Run This Project

### Requirements

You will need:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* scikit-learn
* Jupyter Notebook

### Steps

1. Clone or download this repository.
2. Open the project in Jupyter Notebook or your preferred Python environment.
3. Open the project notebook.
4. Make sure the required Python libraries are installed.
5. Run the notebook cells in order to reproduce the data cleaning, analysis, visualizations, and Logistic Regression model.

The dataset can be accessed from the source provided in the **Dataset** section.

## What I'd Do Next

If I continued this project, I would:

* Try a different machine learning model.
* Add more relevant features to the analysis.
* Tune the model further to see whether its performance can be improved.
