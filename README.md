# 🎓 Statistical Analysis and Machine Learning-Based Prediction of Student Dropout

## 📌 Project Overview

Student dropout is a major challenge for educational institutions, affecting students' academic progress and institutional graduation rates.

This project focuses on analyzing student dropout patterns and predicting whether a student is likely to drop out using demographic, socio-economic, behavioural, and academic performance data.

The project applies **Exploratory Data Analysis (EDA), Statistical Analysis, Hypothesis Testing, and Machine Learning Classification** to identify the key factors associated with student dropout and evaluate different predictive models.

## 🎯 Objectives

- Analyze student academic, demographic, behavioural, and socio-economic information.
- Identify patterns and trends associated with student dropout.
- Perform statistical analysis to understand the relationship between different factors and dropout.
- Apply hypothesis testing to determine statistically significant factors.
- Develop and compare multiple machine learning classification models.
- Evaluate model performance using appropriate classification metrics.
- Identify important features that contribute to student dropout prediction.

## 📊 Dataset Description

The project uses a student dropout dataset containing:

- **Total Records:** 10,000 students
- **Total Features:** 19 columns

The dataset includes the following categories:

| Category | Features |
|---|---|
| Demographic | Age, Gender, Parental Education |
| Socio-Economic | Family Income, Internet Access, Scholarship, Part-Time Job |
| Behavioural | Study Hours, Attendance Rate, Assignment Delay, Travel Time, Stress Index |
| Academic | GPA, Semester GPA, CGPA, Semester, Department |
| Target Variable | Dropout |

**Target Variable: `Dropout`**

- `0` – Not Dropout
- `1` – Dropout

## 🛠️ Technologies & Libraries Used

- **Programming Language:** Python
- **Development Environment:** Google Colab / Jupyter Notebook
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Statistical Analysis:** SciPy
- **Machine Learning:** Scikit-learn

## ⚙️ Project Workflow

### 1. Data Loading and Inspection
- Load the student dataset using Pandas.
- Examine dataset dimensions, data types, and feature names.
- Identify missing values and duplicate records.
- Inspect the distribution of the target variable.

### 2. Data Preprocessing
- Remove the unique `Student_ID` column.
- Handle missing numerical values using median imputation.
- Replace missing categorical values in `Parental_Education` with `Unknown`.
- Verify data quality after preprocessing.

### 3. Exploratory Data Analysis (EDA)
- Analyze numerical and categorical variables.
- Study dropout distribution across different departments and semesters.
- Visualize relationships between academic performance, attendance, stress, and dropout.
- Generate correlation heatmaps and other visualizations.

### 4. Statistical Analysis
The following statistical techniques are implemented:

- Descriptive Statistics
- 95% Confidence Interval for Dropout Rate
- Independent Welch's T-Test
- Mann-Whitney U Test
- Chi-Square Test of Independence
- Correlation Analysis

A significance level of **α = 0.05** is used for hypothesis testing.

### 5. Machine Learning Model Development

The target variable is `Dropout`, which makes this a binary classification problem.

The following models are implemented and compared:

1. Logistic Regression
2. Decision Tree Classifier
3. K-Nearest Neighbors (KNN)
4. Gaussian Naive Bayes
5. Random Forest Classifier

An 80:20 stratified train-test split is used for model training and evaluation.

Categorical variables are one-hot encoded, and numerical features are standardized.

### 6. Model Evaluation

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Macro F1-Score
- ROC-AUC Score
- Confusion Matrix
- ROC Curves

A majority-class baseline model is also implemented to compare the performance of the trained classifiers.

### 7. Feature Importance

Logistic Regression coefficients and Random Forest feature importance are analyzed to identify the most influential predictors of student dropout.

## 📈 Key Findings

The analysis produced the following findings:

- The overall student dropout rate is approximately **23.5%**.
- Academic performance indicators such as GPA, Semester GPA, and CGPA show strong negative correlations with dropout.
- Stress Index shows a positive association with dropout.
- Attendance Rate is negatively associated with dropout.
- Internet Access and Part-Time Job show statistically significant associations with dropout.
- Gender, Scholarship, Semester, Department, and Parental Education do not show statistically significant associations with dropout in this dataset.

### Machine Learning Results

**Logistic Regression** was selected as the primary model based on its overall balanced classification performance.

| Evaluation Metric | Result |
|---|---:|
| Accuracy | ~74.5% |
| ROC-AUC | ~0.82 |
| F1-Score (Dropout) | ~0.583 |

Logistic Regression demonstrated the strongest overall balance, particularly in identifying students belonging to the dropout class.

## 📸 Project Results and Visualizations

![Student Dropout Prediction Results](student_dropout_results_collage.png)

**Important Features Identified:**
- GPA
- Attendance Rate
- Stress Index
- Assignment Delay Days
- Part-Time Job

## 📁 Project Structure

```text
Student-Dropout-Prediction/
│
├── Student_Dropout_Prediction.ipynb
├── data.csv
└── README.md
```

*Note: The dataset file should be added only if you have permission to redistribute it.*

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/Student-Dropout-Prediction.git
```

### Step 2: Navigate to the Project Folder

```bash
cd Student-Dropout-Prediction
```

### Step 3: Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn scipy scikit-learn
```

### Step 4: Add the Dataset

Place the dataset file named `data.csv` in the project directory.

### Step 5: Run the Notebook

Open the notebook using Jupyter Notebook or Google Colab and execute all cells sequentially.

## ⚠️ Limitations

- Missing-value imputation may introduce some simplifications into the analysis.
- Academic performance variables such as GPA, Semester GPA, and CGPA are highly correlated.
- Statistical associations do not establish causation.
- The findings are specific to the dataset and may not generalize to every educational institution.
- Class imbalance may affect the classification performance of individual models.

## 🔮 Future Enhancements

- Develop an interactive student dropout prediction dashboard.
- Explore additional machine learning and ensemble techniques.
- Improve dropout detection through hyperparameter tuning.
- Incorporate explainable AI techniques for better model interpretability.
- Develop an early-warning system to help educational institutions identify at-risk students.

