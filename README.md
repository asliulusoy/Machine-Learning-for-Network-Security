# Machine Learning for Network Security

## How to Run?

* mid.ipynb: Jupyter Notebook containing the Python code.
* README.md: Documentation file providing an overview of the project and instructions on running the code.

To run the code, follow these steps:

@todo: nasıl çalıştıracağını açıkla


## Overview
This repository contains code for implementing machine learning techniques for network security using Python. The code is organized into different sections for data preprocessing, exploratory data analysis (EDA), and applying data mining techniques. It leverages popular libraries such as pandas, scikit-learn, matplotlib, and seaborn.

**Data Preprocessing:** The first step involves data preprocessing where missing values are handled, duplicate rows are removed, and feature selection is performed. The code reads CSV files from Google Drive, concatenates them into one dataframe, and applies preprocessing techniques such as handling missing values, removing duplicates, and dropping constant columns.

**Exploratory Data Analysis (EDA):** After preprocessing, exploratory data analysis is conducted to gain insights into the dataset. This includes computing descriptive statistics, visualizing the correlation matrix, plotting distributions of features, and analyzing feature importance using RandomForestClassifier.

**Applying Data Mining Techniques:** In this section, a machine learning model (K-Nearest Neighbors) is trained and evaluated using the preprocessed data. The dataset is split into training and testing sets, features are scaled, and the KNN model is trained. Evaluation metrics such as accuracy score, classification report, and confusion matrix are computed to assess the model's performance.

@todo: neden bu modeli seçtiğimizi anlat.

### Data Preprocessing
The purpose of this section is to prepare the dataset for further analysis and modeling by handling missing values, removing duplicates, and performing feature selection.
```
from google.colab import drive
drive.mount('/content/drive')
import os
os.chdir("drive/MyDrive/MTH_410/MachineLearningCSV/MachineLearningCVE")
```
This code mounts Google Drive to access files and changes the working directory to the location where the dataset CSV files are stored.

```
files = os.listdir()
data = pd.concat(map(pd.read_csv, files), ignore_index=True)
```
The code reads all CSV files from the specified directory using os.listdir() and then concatenates them into a single dataframe using pd.concat(). This ensures that all data from multiple files are combined into one dataframe for analysis.
```
data.columns[data.isnull().any()]
data = data.replace([np.inf, -np.inf], np.nan)
data.dropna(inplace=True)
```
These lines of code identify columns that contain missing values by using data.isnull().any(). Then, it replaces infinite values (if any) with NaN using data.replace() and drops rows with NaN values using data.dropna(). This ensures that the dataset does not contain any missing or infinite values.
```
for col in data.columns:
    if data[col].nunique() == 1:
        data.drop(col, inplace=True, axis=1)
```
This code snippet drops columns where all values are the same, also known as constant columns. It iterates through each column in the dataframe, checks the number of unique values using data[col].nunique(), and drops columns with only one unique value using data.drop(). This helps in reducing redundancy and improving computational efficiency.
### Exploratory Data Analysis (EDA)
...

### Applying Data Mining Techniques
...

## Requirements
@todo:requirements.txt oluştur ve buraya dahil et.

## Dataset
The dataset used in this project contains network traffic data for security analysis. It includes various features related to network traffic, such as packet length, flow packets, and labels indicating different types of network attacks.

References
pandas Documentation
scikit-learn Documentation
matplotlib Documentation
seaborn Documentation

## Contributors
@asliulusoy asligizemulusoy@gmail.com
