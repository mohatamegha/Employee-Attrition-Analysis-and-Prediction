# Employee-Attrition-Analysis-and-Prediction

## Project Overview
Employee attrition is a critical challenge for organizations. This project analyzes HR data to identify the key factors influencing employee retention and builds a **logistic regression model** to predict whether an employee is likely to leave the company.

The project combines **exploratory data analysis (EDA)** with **machine learning** to derive insights and make predictions based on employee satisfaction, salary, promotions, and workload.

---

## Dataset Description
The dataset contains **14,999 employee records** with the following attributes:

- satisfaction_level  
- last_evaluation  
- number_project  
- average_montly_hours  
- time_spend_company  
- Work_accident  
- promotion_last_5years  
- Department  
- salary  
- left  

**Target Variable**
- `left` → 1 if employee left the company, 0 otherwise

---

## Exploratory Data Analysis (EDA)

### Key Insights
- Employees who left had **significantly lower satisfaction levels** compared to those who stayed.
- Employees who worked **longer average monthly hours** were more likely to leave.
- Employees who received **promotions in the last 5 years** were more likely to stay.
- **Salary** strongly influences attrition:
  - Low salary → highest attrition
  - High salary → lowest attrition
- Department showed minimal influence and was excluded from modeling.

---

## Feature Selection
Based on EDA results, the following features were selected:

- `satisfaction_level`
- `promotion_last_5years`
- `average_montly_hours`
- `salary` (one-hot encoded)

Excluded features:
- last_evaluation  
- number_project  
- time_spend_company  
- Work_accident  
- Department  

---

## Data Preprocessing
- Selected relevant features
- Applied **one-hot encoding** to the `salary` column
- Split the dataset into:
  - 80% training data
  - 20% testing data

---

## Model Building
- Model Used: **Logistic Regression**
- Parameter: `max_iter = 1000`

The model was trained to predict the probability of employee attrition.

---

## Model Evaluation

### Test Set Accuracy
0.762

### Confusion Matrix
[[2124 170]
[ 544 162]]

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
