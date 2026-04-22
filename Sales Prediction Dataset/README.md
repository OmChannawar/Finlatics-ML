# 📈 Sales Prediction Using Advertising Data

This project was completed as part of the **Machine Learning Course by Finlatics**.  
The objective of this project is to analyze how advertising budgets across different media channels influence product sales and to build a **machine learning model that predicts sales based on advertising expenditure**.

---

## 📌 Project Overview

Companies spend large amounts on advertising through different platforms such as **TV, Radio, and Newspapers**. Understanding how these investments affect product sales helps businesses make better marketing decisions.

In this project, **Exploratory Data Analysis (EDA)** and **Multiple Linear Regression** are used to study the relationship between advertising spending and sales performance.

---

## 📊 Dataset Description

The dataset contains advertising spending information and corresponding product sales.

| Feature | Description |
|------|------|
| TV | Advertising budget spent on TV |
| Radio | Advertising budget spent on Radio |
| Newspaper | Advertising budget spent on Newspaper |
| Sales | Number of product units sold |

---

## 🎯 Project Objectives

- Analyze advertising spending patterns
- Understand the relationship between advertising channels and sales
- Build a **machine learning model to predict sales**
- Compare model performance before and after **data normalization**
- Evaluate the effect of different advertising channels on predictions

---

## ⚙️ Project Workflow

### 1. Data Analysis
- Calculated the **average advertising spending on TV**
- Examined the **correlation between Radio advertising and Sales**
- Identified which advertising medium has the strongest impact on sales

### 2. Model Building
Built a **Multiple Linear Regression model** using:
- TV advertising budget
- Radio advertising budget
- Newspaper advertising budget

### 3. Model Evaluation
- Visualized **Actual vs Predicted Sales**
- Evaluated how accurately the model predicts sales

### 4. Sales Prediction
Predicted product sales for the following advertising campaign:

| TV | Radio | Newspaper |
|----|------|-----------|
| 200 | 40 | 50 |

### 5. Feature Scaling
- Applied **Normalization** to the dataset
- Compared model performance with normalized features

### 6. Feature Selection
- Built an additional model using only **Radio and Newspaper** as predictors

---

## 🧠 Machine Learning Technique

The project uses **Multiple Linear Regression**, which models the relationship between multiple independent variables and a dependent variable.

Sales is predicted using advertising budgets as input features.

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📁 Repository Contents

This repository contains:

- **Sales_Prediction.ipynb** – Jupyter Notebook containing the full analysis and machine learning implementation  
- **dataset.csv** – Advertising dataset used in the project  
- **Sales_Prediction_Report.pdf** – A short report summarizing insights from the analysis  
- **README.md** – Project documentation  

---

## 📌 Key Insights

- Advertising expenditure significantly influences product sales.
- Some advertising channels contribute more strongly to sales predictions.
- Feature scaling can influence regression model performance.
- Using fewer predictors changes the model's predictive capability.

---

## 🙏 Acknowledgements

I would like to thank **Finlatics** for providing the opportunity to work on this machine learning project as part of their ML course.  
The dataset used in this project is a commonly used advertising dataset for learning regression analysis and machine learning concepts.

---

## © Copyright

© 2026 **Om Channawar**

This project is created for educational purposes as part of the **Finlatics Machine Learning Course**.  
The code and documentation in this repository may be used for learning and reference purposes with proper attribution.

---

## 👨‍💻 Author

**Om Channawar**  
Machine Learning Project – Finlatics ML Course