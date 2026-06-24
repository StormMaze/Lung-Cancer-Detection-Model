# Lung Cancer Detection Using ML

## Overview

Early detection of lung cancer can significantly improve treatment outcomes and survival rates. This project explores the use of ML techniques to predict the likelihood of lung cancer based on patient symptoms, habits and medical conditions collected through a survey dataset.

The objective of this project is to analyze the factors associated with lung cancer and compare the performance of different predictive models. Both regression and classification approaches were implemented using **Linear Regression** and **K-Nearest Neighbors (KNN)** to understand how effectively they can identify potential lung cancer cases.


## Dataset

The project uses the **Lung Cancer Survey Dataset**, which contains information collected from 309 individuals. The dataset includes demographic details, lifestyle habits, symptoms and medical conditions that may contribute to lung cancer risk.

The target variable indicates whether a person has lung cancer:

**YES** – Diagnosed with lung cancer  **NO** – Not diagnosed with lung cancer


## Features Used

| Feature               | Description                          |
| --------------------- | ------------------------------------ |
| Gender                | Male (M) or Female (F)               |
| Age                   | Age of the individual                |
| Smoking               | Smoking habit                        |
| Yellow Fingers        | Presence of yellowstained fingers   |
| Anxiety               | Anxiety condition                    |
| Peer Pressure         | Influence of peers on smoking habits |
| Chronic Disease       | Presence of chronic disease          |
| Fatigue               | Persistent tiredness                 |
| Allergy               | Allergy related issues               |
| Wheezing              | Breathing difficulties               |
| Alcohol Consuming     | Alcohol consumption habit            |
| Coughing              | Frequent coughing                    |
| Shortness of Breath   | Difficulty breathing                 |
| Swallowing Difficulty | Trouble swallowing                   |
| Chest Pain            | Presence of chest pain               |
| Lung Cancer           | Target variable (YES/NO)             |

Most categorical variables are encoded as:

* YES = 2 * NO = 1


## Technologies Used

* Python
* Pandas
* Scikit-learn
* Matplotlib

### Installation

Install the required dependencies using:

```bash
pip install pandas scikit-learn matplotlib
```

---

## Project Structure

```text
├── LungCancerDetection.ipynb
├── lung_cancer.csv
└── README.md
```

### Files Description

* **LungCancerDetection.ipynb** – Jupyter Notebook containing data preprocessing, model training, evaluation, and visualization.
* **lung_cancer.csv** – Dataset used for training and testing the models.
* **README.md** – Project documentation.


## Methodology

### 1. Data Preprocessing

Before training the models, the dataset undergoes several preprocessing steps:
* Encoding categorical variables
* Feature scaling
* Data splitting into training and testing sets
* Transformation using Scikit learn's preprocessing tools


### 2. Linear Regression

Linear Regression was implemented to study relationships between features and the target variable.

Evaluation Metrics:
* Root Mean Squared Error (RMSE)
* Mean Absolute Error (MAE)

A feature coefficient (loadings) plot was also generated to visualize the impact of different variables on the prediction.


### 3. K-Nearest Neighbors Regression

KNN Regression predicts outcomes based on the similarity of neighboring data points.

Key Steps:
* Hyperparameter tuning using **GridSearchCV**
* Selection of optimal value of **K**
* Model training and evaluation

Evaluation Metrics:
* RMSE
* MAE

### 4. K-Nearest Neighbors Classification

KNN Classification was used to classify whether a patient is likely to have lung cancer.

Evaluation Metrics:
* Accuracy
* Precision
* Recall
* F1-Score
* Sensitivity
* Specificity

These metrics provide a detailed understanding of the model's ability to correctly identify both positive and negative cases.


## Running the Project

### Step 1: Download the Project

Clone the repository or download the project files.

```bash
git clone https://github.com/StormMaze/Lung-Cancer-Detection-Model.git
```

Make sure the dataset file i.e survey ' lung_cancer.csv ' is placed in the same directory as the notebook.


### Step 2: Run the Notebook

Open the notebook and execute all cells:

```bash
jupyter notebook LungCancerDetection.ipynb
```

The notebook will:
* Load and preprocess the dataset
* Train the machine learning models
* Tune hyperparameters
* Evaluate performance
* Generate visualizations


### Step 3: Review Results

After execution, review:
* Model performance metrics
* Feature importance plots
* Classification results
* Comparative analysis between models


## Results and Observations

### Linear Regression
* Produced stable and consistent predictions.
* Achieved lower RMSE values compared to other approaches.
* Suitable when overall prediction stability is important.

### KNN Regression
* Delivered lower MAE values.
* Demonstrated better local prediction accuracy.
* Effective when predictions depend heavily on neighboring data points.

### KNN Classification
* Achieved high accuracy and recall.
* Successfully identified most positive lung cancer cases.
* High recall makes it useful for early detection applications.
* Lower specificity indicates a tendency toward false positives, suggesting further optimization may improve performance.


## Key Insights

* Symptoms such as coughing, chest pain, wheezing, and shortness of breath show strong associations with lung cancer prediction.
* KNN-based approaches perform well due to their ability to capture local patterns within the dataset.
* High recall is particularly valuable in healthcare applications because missing a positive cancer case can have serious consequences.


## Conclusion

This project demonstrates how machine learning can be applied to assist in the early prediction of lung cancer using survey based health data.

The comparison between Linear Regression and K-Nearest Neighbors shows that each model has its own strengths:
* **Linear Regression** provides more stable and consistent predictions.
* **KNN Regression** offers improved prediction precision.
* **KNN Classification** achieves strong detection performance with high recall, making it suitable for identifying potential lung cancer cases.

Although the models show promising results, further improvements can be made by using larger datasets, advanced feature engineering techniques and more sophisticated machine learning algorithms.

---

## Future Scope

* Explore ensemble models such as Random Forest and XGBoost.
* Perform feature selection to identify the most influential risk factors.
* Use larger medical datasets for improved generalization.
* Develop a web based application for real-time lung cancer risk assessment.
* Integrate explainable AI techniques for better medical interpretability.

---

## Author

**Subham Mohakud**
Computer Science & Engineering
Siksha 'O' Anusandhan University (ITER)

Machine Learning Project – Lung Cancer Prediction
