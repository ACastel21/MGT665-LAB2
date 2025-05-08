# MGT665-LAB2
# Performance Classification Lab

This project demonstrates the use of machine learning classification models to predict student performance based on various features. The dataset used is the **Students Performance Dataset**, which is publicly available on Kaggle.

## Overview

The notebook builds and evaluates three classification models:
- **Logistic Regression**
- **k-Nearest Neighbors (k-NN)**
- **Decision Tree**

The models are trained and tested on a dataset of student performance metrics, and their results are compared using classification metrics and confusion matrices.


## Dataset Details

The dataset contains information about students' academic performance and other related attributes. Below are the details:

- **Source**: [Students Performance Dataset on Kaggle](https://www.kaggle.com/datasets/rabieelkharoua/students-performance-dataset)
- **Number of Rows**: 1000 (each row represents a student)
- **Number of Columns**: 8 (including the target variable)

### Features:
- **StudentID**: A unique identifier for each student (irrelevant for modeling).
- **Gender**: The gender of the student (e.g., Male, Female).
- **Race/Ethnicity**: The race/ethnicity group of the student.
- **Parental Level of Education**: The highest level of education achieved by the student's parents.
- **Lunch**: Whether the student receives free/reduced lunch or standard lunch.
- **Test Preparation Course**: Whether the student completed a test preparation course.
- **Math Score**: The student's score in the math test.
- **Reading Score**: The student's score in the reading test.
- **Writing Score**: The student's score in the writing test.

### Target Variable:
**GradeClass**: The classification of the student's overall performance (e.g., Low, Medium, High).



## Steps in the Notebook

### 1. **Retrieve Dataset**
The dataset is downloaded from Kaggle using the `kagglehub` package. The file is stored locally for further processing.

### 2. **Preprocessing**
- Irrelevant columns (`StudentID`, `GPA`, etc.) are dropped.
- Features are scaled using `StandardScaler` to improve model performance.
- The dataset is split into training (80%) and testing (20%) sets.

### 3. **Exploratory Data Analysis**
- Visualizations include:
  - Distribution of the target variable (`GradeClass`).
  - Pairplots to explore relationships between features.
  - Heatmap to analyze feature correlations.

### 4. **Model Development and Evaluation**
Three models are trained and evaluated:
- **Logistic Regression**: A simple and interpretable model that works well for linearly separable data.
- **k-Nearest Neighbors (k-NN)**: A distance-based model that relies on the choice of `k` and data scaling.
- **Decision Tree**: A tree-based model that captures complex patterns but may overfit.

Each model's performance is evaluated using:
- Classification reports (precision, recall, F1-score).
- Confusion matrices to visualize prediction errors.

### 5. **Discussion**
- **Logistic Regression**: Achieved the highest accuracy. It is fast, interpretable, and effective for this dataset.
- **k-NN**: Showed slightly lower performance. Its results depend on the choice of `k` and data scaling.
- **Decision Tree**: Provided decent results but is prone to overfitting. It offers interpretability and can handle both numerical and categorical data.

### 6. **Confusion Matrices**
Confusion matrices are plotted for each model to visualize the distribution of true positives, false positives, true negatives, and false negatives.



## Summary of Model Strengths and Weaknesses

### Logistic Regression:
- **Strengths**: High accuracy, fast, interpretable, and effective for linearly separable data.
- **Weaknesses**: May struggle with non-linear relationships or high-dimensional data.

### k-Nearest Neighbors (k-NN):
- **Strengths**: Simple to implement and understand.
- **Weaknesses**: Sensitive to the choice of `k` and data scaling. Computationally expensive for large datasets.

### Decision Tree:
- **Strengths**: Captures complex patterns, handles both numerical and categorical data, and is interpretable.
- **Weaknesses**: Prone to overfitting, especially with deeper trees.


