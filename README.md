# 📊 HR Analytics: Job Change Prediction

## 📋 Project Overview
This project addresses a critical challenge in the HR and talent acquisition domain, specifically for a company specializing in Big Data and Data Science training and recruitment. The company provides specialized training programs as part of their recruitment pipeline but faces significant resource allocation challenges due to uncertainty about candidates' post-training intentions.

The project leverages machine learning techniques to analyze candidate data collected during the signup and enrollment processes. By examining various factors including demographics, educational background, work experience, and training participation, we've developed predictive models to identify candidates genuinely interested in joining the company post-training versus those likely to seek employment elsewhere.

Key challenges addressed in this project include:
- Managing an imbalanced dataset reflecting real-world recruitment patterns
- Handling multiple categorical variables with high cardinality
- Processing missing data across several critical features
- Developing a robust pipeline for automated data preprocessing and model training


## 🎯 Project Objectives
- Predict the likelihood of candidates changing jobs after training
- Identify key factors influencing job change decisions
- Optimize training resource allocation
- Reduce recruitment costs and time
- Improve candidate categorization

## 🔍 Dataset Description

### Data Source
- Training set: 19,158 records
- Test set: 2,129 records
- Target variable is binary (0: No job change, 1: Will change job)
- [Dataset on Kaggle](https://www.kaggle.com/arashnic/hr-analytics-job-change-of-data-scientists)

### Features

| Feature | Description |
|---------|-------------|
| enrollee_id | Unique ID for candidate |
| city | City code |
| city_development_index | Development index of the city (scaled) |
| gender | Gender of candidate |
| relevant_experience | Relevant experience of candidate |
| enrolled_university | Type of University course enrolled if any |
| education_level | Education level of candidate |
| major_discipline | Education major discipline of candidate | 
| experience | Candidate total experience in years | 
| company_size | No of employees in current employer's company |
| company_type | Type of current employer | 
| lastnewjob | Difference in years between previous job and current job | 
| training_hours | Training hours completed |
| target | Looking for job change (0: No, 1: Yes) |

## 🛠 Methodology

### Data Preprocessing
- Handled missing values
- Implemented encoding techniques
- Applied feature scaling
- Reduced dimensions using PCA
- Created automated pipelines for preprocessing steps

### Machine Learning Models
Explored multiple classification algorithms:
- Stochastic Gradient Descent
- Logistic Regression
- Linear SVC
- Random Forest Classifier
- Extra Trees Classifier
- Voting Classifier (Ensemble of Logistic Regression, Random Forest, and ExtraTrees)

### Model Evaluation
- Primary metric: ROC-AUC Score (due to class imbalance)
- Secondary metric: Accuracy

## 📊 Results
### Best Model: Soft Voting Classifier
Validation Set Performance:
- Accuracy: 91.01%
- ROC-AUC Score: 93.4%

Test Set Performance:
- Accuracy: 73%
- ROC-AUC Score: 71.49%

## 🚀 Installation

### Prerequisites
- Python 3.8+
- Required libraries:
  ```
  pandas
  numpy
  scikit-learn
  matplotlib
  seaborn
  pickle
  ```

### Setup
```bash
git clone https://github.com/odabashi/HR-Analytics.git
cd HR-Analytics
```

## 📈 Future Improvements
- Implementation of more sophisticated anomaly detection methods
- Feature engineering to improve model performance
- Exploration of deep learning approaches
- Addressing class imbalance by applying over- & undersampling techniques

## 👥 Team Members
| **Team Member** |
|---|
| Baraa ALSALEH |
| Abdurrahman ODABAŞI |
| Muhammed ŞİHEBİ |

<p align="center"> 
    ⭐ Found this project helpful? A quick upvote on Kaggle and star on Github will support continued research and sharing! 👍
</p> 
