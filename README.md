# Alzheimer’s Disease Risk Prediction

This project presents a machine learning workflow for predicting Alzheimer’s disease risk using tabular clinical and demographic data.

## Open in Google Colab
[Open in Google Colab](https://colab.research.google.com/github/zpempera/Alzheimer-s-Disease-Risk-Prediction/blob/main/notebooks/Alzheimer’s_Disease_Risk_Prediction.ipynb) 

## Project overview

The notebook covers the full machine learning pipeline, including:
- data loading and exploration
- preprocessing and feature handling
- class imbalance analysis
- train and test split
- preprocessing pipeline construction
- model selection and hyperparameter tuning
- final evaluation using classification metrics and ROC AUC

The project compares multiple configurations of:
- resampling methods
- dimensionality reduction techniques
- classification algorithms

The final best-performing approach was based on Logistic Regression combined with LDA and oversampling.

## Dataset

Source dataset:
[Kaggle Alzheimer’s Disease Dataset](https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset)

The input data file used in this project is stored in:

`data/raw/alzheimers_disease_data.csv`

## Methodology

The workflow includes:
- checking missing values
- removing the `Ethnicity` column to reduce the risk of biased associations
- examining similarity between selected memory-related variables
- scaling numerical variables
- stratified train and test split
- preprocessing with `ColumnTransformer`
- resampling with SMOTE or RandomOverSampler
- dimensionality reduction with PCA or LDA
- model comparison across Logistic Regression, Perceptron, KNN, and Random Forest
- hyperparameter tuning with `RandomizedSearchCV`

## Evaluation

The final model was evaluated using:
- F1 score
- accuracy
- confusion matrix
- ROC AUC
- learning curve
- validation curve

The results suggest that Logistic Regression with LDA and resampling provided the strongest performance among the tested configurations.

## Project structure

```text
alzheimers-risk-prediction/
├─ README.md
├─ requirements.txt
├─ notebooks/
│  └─ Alzheimer’s_Disease_Risk_Prediction.ipynb
└─ data/
   └─ raw/
      └─ alzheimers_disease_data.csv
