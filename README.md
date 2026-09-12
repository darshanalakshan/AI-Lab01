# IAI600 – Introduction to Applied Artificial Intelligence

## Lab I – Data Exploration, Cleaning and Feature Preparation

This repository contains my work for **Lab I** of the **IAI600 – Introduction to Applied Artificial Intelligence** course.

The laboratory focuses on the first stages of an **end-to-end Machine Learning project** using the **California Housing Dataset**.

---

## 🎯 Objective

The main objective of this laboratory is to develop a practical understanding of how real-world data is explored, cleaned, and prepared before training a machine learning model.

Through this lab, I explore:

* Understanding the dataset
* Exploring data distributions
* Identifying data quality issues
* Investigating relationships between variables
* Handling missing values
* Handling categorical data
* Preparing numerical features
* Scaling numerical features
* Building a preprocessing pipeline

---

## 📊 Dataset

### California Housing Dataset

The dataset contains information about housing districts in California.

Some of the main attributes include:

* `longitude`
* `latitude`
* `housing_median_age`
* `total_rooms`
* `total_bedrooms`
* `population`
* `households`
* `median_income`
* `median_house_value`
* `ocean_proximity`

The target variable for the original machine learning problem is:

```text
median_house_value
```

---

## 🧪 Laboratory Tasks

### 1. Load and Understand the Dataset

* Load the dataset using Pandas
* Examine the dataset structure
* Check the number of observations and attributes
* Identify numerical and categorical attributes
* Inspect basic statistics

### 2. Explore the Data

Data exploration includes:

* Histograms
* Distribution analysis
* Identifying skewed attributes
* Comparing numerical scales
* Detecting unusually large or small values

### 3. Create Training and Test Sets

The dataset is divided into:

* **Training set** – used to train the machine learning model
* **Test set** – used to evaluate the model

The purpose is to prevent the model from being evaluated on the same data used for training.

### 4. Investigate Relationships Between Attributes

Relationships between variables are explored using:

* Correlation analysis
* Scatter plots
* Attribute comparisons
* Geographic visualization

### 5. Handle Missing Values

Missing values are identified and handled appropriately.

For example:

```python
from sklearn.impute import SimpleImputer

imputer = SimpleImputer(strategy="median")
```

### 6. Handle Categorical Attributes

Categorical variables such as:

```text
ocean_proximity
```

are converted into numerical representations suitable for machine learning algorithms.

### 7. Prepare Numerical Attributes

Numerical features are separated and prepared for further processing.

### 8. Feature Scaling

Features with different numerical scales are transformed so that they can be used effectively by machine learning algorithms.

Example:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
```

### 9. Build a Preprocessing Pipeline

A preprocessing pipeline is created using Scikit-learn to organize the data preparation steps.

Example:

```python
from sklearn.pipeline import Pipeline

num_pipeline = Pipeline([
    ("imputer", SimpleImputer(strategy="median")),
    ("scaler", StandardScaler())
])
```

---

## 🛠️ Technologies Used

| Technology       | Purpose                            |
| ---------------- | ---------------------------------- |
| Python           | Programming language               |
| Jupyter Notebook | Data analysis and experimentation  |
| Pandas           | Data manipulation                  |
| NumPy            | Numerical operations               |
| Matplotlib       | Data visualization                 |
| Scikit-learn     | Machine learning and preprocessing |

---

## 📁 Repository Structure

```text
IAI600-Lab-I/
│
├── README.md
├── Lab_I_California_Housing.ipynb
│
├── data/
│   └── housing.csv
│
└── images/
    └── figures/
```

> The exact folder structure may change depending on the notebook and dataset organization.

---

## 📚 Learning Outcomes

After completing this laboratory, I should be able to:

* Understand the structure of a real-world dataset
* Perform basic exploratory data analysis
* Identify data quality problems
* Split data into training and test sets
* Analyze relationships between attributes
* Handle missing values
* Process categorical attributes
* Prepare numerical features
* Apply feature scaling
* Build a Scikit-learn preprocessing pipeline
* Explain **why** each preprocessing step is required before machine learning

---

## 📖 Reference

This laboratory is based on the concepts presented in:

**Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow**
by Aurélien Géron

The laboratory focuses mainly on the **End-to-End Machine Learning Project** workflow.

---

## 🎓 Course

**Course:** IAI600 – Introduction to Applied Artificial Intelligence
**Laboratory:** Lab I – Data Exploration, Cleaning and Feature Preparation
**Dataset:** California Housing Dataset
