# Autism Prediction ML Model

## Overview

This project focuses on predicting the likelihood of Autism Spectrum Disorder (ASD) using Machine Learning techniques on behavioral and demographic screening data.

The notebook demonstrates a complete end-to-end machine learning workflow including:

* Data preprocessing
* Exploratory Data Analysis (EDA)
* Feature engineering
* Handling missing values
* Outlier treatment
* Class imbalance handling using SMOTE
* Model training and evaluation
* Hyperparameter tuning
* Model serialization for inference

The project was developed using Python in Google Colab.

---

# Problem Statement

Autism Spectrum Disorder (ASD) is a developmental condition that affects communication, behavior, and social interaction.

Early screening and prediction can help:

* identify individuals requiring professional assessment
* improve early intervention opportunities
* support healthcare systems with preliminary screening tools

The goal of this project is to build a machine learning model capable of predicting autism likelihood based on screening questionnaire responses and demographic information.

---

# Dataset Information

The dataset contains:

* behavioral screening scores
* demographic features
* medical history information
* autism screening outcomes

### Example Features

| Feature              | Description                 |
| -------------------- | --------------------------- |
| A1_Score - A10_Score | Behavioral screening scores |
| age                  | Age of individual           |
| gender               | Gender                      |
| ethnicity            | Ethnicity information       |
| jundice              | History of jaundice         |
| austim               | Family history of autism    |
| relation             | Relation of respondent      |
| Class/ASD            | Target variable             |

---

# Project Workflow

## 1. Data Loading

The dataset was loaded into a Pandas DataFrame and inspected for:

* missing values
* invalid entries
* inconsistent categories

---

## 2. Data Cleaning

Several preprocessing steps were performed:

* Replaced invalid `?` values
* Standardized categorical values
* Merged duplicate category labels
* Removed unnecessary columns
* Handled outliers using IQR-based methods

---

## 3. Exploratory Data Analysis (EDA)

EDA was performed to better understand:

* feature distributions
* class imbalance
* correlations
* skewness
* categorical feature frequencies

Visualization techniques used:

* Histograms
* Boxplots
* Countplots
* Correlation heatmaps

---

## 4. Feature Engineering

Categorical variables were encoded using `LabelEncoder`.

Features and target variables were separated for training.

---

## 5. Handling Class Imbalance

The dataset showed class imbalance between autism-positive and autism-negative cases.

To address this issue:

* SMOTE (Synthetic Minority Oversampling Technique) was applied to the training data

This improved the model’s ability to learn minority class patterns.

---

# Machine Learning Models Used

The following models were trained and compared:

| Model                    | Purpose                 |
| ------------------------ | ----------------------- |
| Decision Tree Classifier | Baseline tree model     |
| Random Forest Classifier | Ensemble learning       |
| XGBoost Classifier       | Gradient boosting model |

---

# Hyperparameter Tuning

Hyperparameter optimization was performed using:

* `RandomizedSearchCV`
* Cross-validation

This helped improve model performance by searching for better parameter combinations.

---

# Model Evaluation

Models were evaluated using:

* Accuracy Score
* Classification Report
* Confusion Matrix

The best-performing model was selected as the final model.

---

# Model Saving

The trained model and encoders were serialized using `pickle`.

Saved files:

* `best_model.pkl`
* `encoders.pkl`

These files can later be used for:

* inference
* deployment
* API integration

---

# Technologies Used

## Programming Language

* Python

## Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* XGBoost
* Pickle

## Environment

* Google Colab
* Jupyter Notebook

---

# Project Structure

```bash
Autism-Prediction-ML-Model/
│
├── AutismPredictionMLModel.ipynb
├── autism_dataset.csv
├── best_model.pkl
├── encoders.pkl
└── README.md
```

---

# Key Learnings From This Project

This project helped strengthen understanding of:

* End-to-end ML workflows
* Data preprocessing techniques
* EDA practices
* Handling imbalanced datasets
* Hyperparameter tuning
* Model comparison
* ML inference pipeline creation

---

# Future Improvements

Planned improvements include:

* Using `OneHotEncoder` and `Pipeline`
* Deploying model using Flask/FastAPI
* Building Streamlit web interface
* Improving evaluation with ROC-AUC and F1 optimization
---

# Disclaimer

This project is intended for educational and research purposes only.
