# Random Forest Breast Cancer Classification

## Project Overview

This project applies a **Random Forest Classifier** to a breast cancer classification dataset. The analysis focuses on identifying the most important features for classification and evaluating model performance using different combinations of selected features.

The notebook was developed in **Google Colab** using Python and common machine learning and data analysis libraries.

## Dataset

The dataset contains **569 observations and 32 columns**. The target variable is `diagnosis`, which is encoded for machine learning.

The dataset includes measurements such as:

* Radius
* Texture
* Perimeter
* Area
* Smoothness
* Compactness
* Concavity
* Concave points
* Symmetry
* Fractal dimension

The variables are provided in different forms, including:

* Mean measurements
* Standard error (`se`) measurements
* Worst measurements

## Technologies and Libraries

The project uses:

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Google Colab

## Data Preparation

The notebook performs several preprocessing steps:

1. Loads the dataset from a CSV file.
2. Removes unnecessary `Unnamed` columns.
3. Removes rows containing missing values.
4. Encodes the `diagnosis` variable using `LabelEncoder`.
5. Separates the predictor variables from the target variable.

## Machine Learning Model

A **Random Forest Classifier** is used to classify the observations based on the available features.

Random Forest is also used to determine the relative importance of individual features in the classification process.

## Feature Importance Analysis

The model calculates feature importance scores to identify the variables that contribute most to the classification.

The analysis identifies features such as:

* `area_worst`
* `radius_worst`
* `concave points_worst`
* `perimeter_worst`
* `concave points_mean`

among the important features.

The notebook then examines the top features and compares their performance with other feature combinations.

## Model Evaluation

The project evaluates different feature combinations using:

* Accuracy
* Recall
* Precision
* F1 Score

Three feature-selection approaches are considered:

1. **Top 5 features**
2. **Last 5 features**
3. **Mixed feature combinations**

This allows the performance of different feature sets to be compared rather than relying only on the complete dataset.

## Project Structure

```text
Random_Forest_Breast_Cancer_Classification/
│
├── Random_Forest_Breast_Cancer_Classification.ipynb
├── README.md
└── dataset.csv
```

> Replace `dataset.csv` with the actual name of your CSV file if it has a different filename.

## How to Run

### Google Colab

1. Open the `.ipynb` notebook in Google Colab.
2. Upload the required CSV dataset when prompted.
3. Run the notebook cells sequentially.
4. Review the feature-importance results and model evaluation metrics.

### Local Jupyter Environment

Install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

Then open:

```text
Random_Forest_Breast_Cancer_Classification.ipynb
```

and execute the notebook cells.

## Results

The notebook produces:

* Dataset information
* Encoded target values
* Random Forest feature-importance rankings
* Top feature selections
* Model performance for different feature combinations
* Accuracy, recall, precision, and F1-score comparisons

## Purpose

The main purpose of this project is to demonstrate how **Random Forest classification and feature importance analysis** can be used to investigate which variables contribute most to classification performance in a breast cancer dataset.
