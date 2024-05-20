# Machine Learning for Network Security

## How to Run?

* mid.ipynb: Jupyter Notebook containing the Python code.
* README.md: Documentation file providing an overview of the project and instructions on running the code.

To run the code, follow these steps:

@todo: nasıl çalıştıracağını açıkla


## Overview
This repository contains code for implementing machine learning techniques for network security using Python. The code is organized into different sections for data preprocessing, exploratory data analysis (EDA), and applying data mining techniques. It leverages popular libraries such as pandas, scikit-learn, matplotlib, and seaborn.

**Data Preprocessing:**

The first step involves data preprocessing where missing values are handled, duplicate rows are removed, and feature selection is performed. The code reads CSV files from Google Drive, concatenates them into one dataframe, and applies preprocessing techniques such as handling missing values, removing duplicates, and dropping constant columns.

**Exploratory Data Analysis (EDA):** 

After preprocessing, exploratory data analysis is conducted to gain insights into the dataset. This includes computing descriptive statistics, visualizing the correlation matrix, plotting distributions of features, and analyzing feature importance using RandomForestClassifier.

**Applying Data Mining Techniques:**

In this section, a machine learning model (K-Nearest Neighbors) is trained and evaluated using the preprocessed data. The dataset is split into training and testing sets, features are scaled, and the KNN model is trained. Evaluation metrics such as accuracy score, classification report, and confusion matrix are computed to assess the model's performance.

* KNN, with a **0.99** accuracy score, was chosen for analyzing the CICIDS2017 dataset due to its simplicity, effectiveness, and transparency, crucial for cybersecurity tasks.
* PCA reduced the dataset to 7 principal components, enhancing KNN's performance in managing high-dimensional data and multi-class classification.
* In comparison, Random Forest (RF) achieved **0.94** accuracy, showing robustness in handling complex datasets.
* Despite a lower accuracy of **0.13**, Gaussian Naive Bayes (GNB) is still relevant for its simplicity and speed.
* Together, these models provide a comprehensive analysis of network traffic, with **KNN being the most accurate and interpretable for intrusion detection and anomaly recognition.**

## Steps

1. **Mount Google Drive to Access Files**
2. **List Files in Directory**
3. **Import Necessary Libraries**
4. **Load and Concatenate CSV Files into a Single DataFrame**
5. **Print the Number of Rows and Columns in the Data**
6. **Remove Duplicate Rows**
7. **Clean Column Names**
8. **Handle Missing and Infinite Values**
9. **Drop Columns with Constant Values**
10. **Reset DataFrame Index**
11. **Perform PCA**
12. **Exploratory Data Analysis (EDA)**
13. **Feature Importance Analysis with RandomForestClassifier**
14. **Additional Scatter Plot and Box Plot for EDA**
15. **Split Data into Training and Testing Sets and Scale Features**
16. **Train and Evaluate KNN Model**
17. **Train and Evaluate Random Forest Model**
18. **Train and Evaluate Naive Bayes Model**
19. **Display Unique Labels and Model Accuracies**


## Requirements
@todo:requirements.txt oluştur ve buraya dahil et.

## Dataset
The dataset used in this project contains network traffic data for security analysis. It includes various features related to network traffic, such as packet length, flow packets, and labels indicating different types of network attacks.

## Contributors
@asliulusoy asligizemulusoy@gmail.com

@emreyd emreyildizh@gmail.com

@Berkayalpay berkayalpay08@gmail.com
