# Classification Challenge

## Project Overview
This project focuses on developing a supervised machine learning model to classify emails as **spam** or **not spam**. The goal is to improve the email filtering system for an Internet Service Provider (ISP) by accurately detecting spam emails. Two classification models are implemented and compared:

1. **Logistic Regression**
2. **Random Forest Classifier**

The [Spam Email Dataset](https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv) includes email features and a binary target variable (`spam`), where:
- `0` indicates a legitimate email.
- `1` indicates a spam email.

## Technologies Used
This project is implemented using **Jupyter Notebook** and relies on the following Python libraries:

- `pandas` - For data manipulation and analysis
- `scikit-learn`:
  - `train_test_split` - To split the dataset into training and testing sets
  - `accuracy_score` - To evaluate model performance
  - `LogisticRegression` - For logistic regression modeling
  - `RandomForestClassifier` - For random forest modeling

## Installation & Setup
To run this project, follow these steps:

1. **Clone the repository** to your local machine:
   ```sh
   git clone https://github.com/jesseparent/classification-challenge.git
   ```

2. **Install dependencies** using `pip`:
   ```sh
   pip install pandas scikit-learn jupyterlab
   ```
3. **Open Jupyter Notebook** and run the notebook:
   ```sh
   jupyter lab
   ```

## File Descriptions
- **`spam_detector.ipynb`** - The main Jupyter Notebook containing:
  - Data preprocessing (loading data, feature/label selection, data splitting)
  - Feature scaling using `StandardScaler`
  - Model training and evaluation (Logistic Regression & Random Forest)
  - Model comparison and analysis

## Methodology

### **1. Split the Data into Training and Testing Sets**
- Load the dataset into a Pandas DataFrame.
- Define **features (X)** and **labels (y)** (`spam` column).
- Check the class balance using `value_counts()`.
- Split the data into **training (80%)** and **testing (20%)** sets using `train_test_split()`.

### **2. Scale the Features**
- Apply `StandardScaler` to normalize the feature data.
- Transform both training and testing feature sets.

### **3. Train and Evaluate Logistic Regression Model**
- Train a **Logistic Regression** model with `random_state=1`.
- Make predictions on the test dataset.
- Evaluate accuracy using `accuracy_score()`.

### **4. Train and Evaluate Random Forest Model**
- Train a **Random Forest Classifier** with `random_state=1`.
- Make predictions on the test dataset.
- Evaluate accuracy using `accuracy_score()`.

### **5. Model Evaluation & Comparison**
- **Logistic Regression Accuracy:** **92.79%**
- **Random Forest Accuracy:** **96.70%**

### **Which Model Performed Better?**
- The **Random Forest Classifier outperformed Logistic Regression** with a higher accuracy score.
- This suggests that the dataset contains **non-linear patterns** that Random Forest captured more effectively.

## How to Use
- Run all cells in `spam_detector.ipynb` to execute the classification models.
- Evaluate accuracy scores of each model.

---

