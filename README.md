# Fraud Detection Task

## Here is the link for the dataset : 

https://drive.usercontent.google.com/download?id=1VNpyNkGxHdskfdTNRSjjyNa5qC9u0JyV&export=download&authuser=0

---

## Online Payments Fraud Detection

This project focuses on building a machine learning model to detect fraudulent transactions in a large-scale financial dataset. The goal is to develop an effective classifier that can identify fraudulent behavior in online payments, providing actionable insights for prevention.

---

## Dataset

The project utilizes a synthetic dataset generated by the PaySim simulator, which mimics mobile money transactions. The dataset contains over 6.3 million records and includes features such as:

* Transaction type (`CASH-IN`, `CASH-OUT`, `DEBIT`, `PAYMENT`, `TRANSFER`)
* Transaction amount
* Account balances before and after the transaction
* A binary label `isFraud` indicating whether the transaction was fraudulent

The fraudulent behavior simulated in the dataset involves attempts to drain account funds by transferring them to another account and then cashing out.

---

## Methodology

1.  **Data Cleaning & Exploration**: The dataset was analyzed for missing values and statistical distributions. Key features were examined to understand the underlying data structure.
2.  **Feature Engineering**: The categorical `type` column was transformed into a numerical format using one-hot encoding.
3.  **Modeling**: A **Random Forest Classifier** was trained on the data. This model was chosen for its high performance on complex datasets and its ability to handle imbalanced classes.
4.  **Evaluation**: The model's performance was assessed using a confusion matrix, precision, and recall scores, which are more informative than accuracy for imbalanced fraud data.

---

## Key Results

* The model achieved a **precision of 0.98** and a **recall of 0.78** for the fraud class, indicating high accuracy in predictions and a strong ability to identify actual fraudulent transactions.
* The most significant predictors of fraud were identified as `oldbalanceOrg` (the sender's initial balance), `amount`, `newbalanceOrig` (the sender's new balance), and `type_TRANSFER`.
* The findings confirm that the model successfully learned to identify the primary fraud pattern: emptying an account via a large transfer.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
