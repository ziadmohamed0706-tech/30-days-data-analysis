# 📅 Day 01 – Data Science Foundations

## 🧠 What I Learned
- 🔍 Data Science = Turning **data → information → insights → right decisions**  
- 🛠️ Core Components:
  - 👨‍💻 **Hacking Skills (Programming, Tools)**
  - 📊 **Math & Statistics**
  - 🌍 **Domain Knowledge**
- 🔄 Data Science Workflow:
  1️⃣ Problem Definition  
  2️⃣ Data Collection & Pre-processing  
  3️⃣ Data Analysis  
  4️⃣ Data Visualization  
  5️⃣ Machine Learning  
  6️⃣ AI Applications  

---

## 📊 Case Study: *E-Commerce Customers*
**Dataset:** [Kaggle – Ecommerce Customers](https://www.kaggle.com/srolka/ecommerce-customers)  

### 🔧 Steps
1. **Importing Libraries**
     ```python
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt
   import seaborn as sns
   from sklearn.model_selection import train_test_split
   from sklearn.linear_model import LinearRegression
   from sklearn.metrics import mean_absolute_error, mean_squared_error
   
2. **Data Loading & Inspection**
     ```python
   ecom = pd.read_csv('datasets/ecommerce-customers.csv')
   ecom.head()
   ecom.info()
   ecom.describe().round(1)

3. **Data Loading & Inspection**
   -📈 Pairplots & Jointplots (relationships between features)
   -🔗 Strong correlation found: Length of Membership ↔ Yearly Amount Spent
  ```python
  X = ecom[['Avg. Session Length','Time on App','Time on Website','Length of Membership']]
  y = ecom['Yearly Amount Spent']
  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)

4. **Train/Test Split**
    ```python
   X = ecom[['Avg. Session Length','Time on App','Time on Website','Length of Membership']]
   y = ecom['Yearly Amount Spent']
   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)

5. **Model Building**
    ```python
   lm = LinearRegression()
   lm.fit(X_train, y_train)

6. **Predictions & Evaluation**
    ```python
   y_pred = lm.predict(X_test)
   print("MAE:", mean_absolute_error(y_test, y_pred))
   print("RMSE:", np.sqrt(mean_squared_error(y_test, y_pred)))


##✅ Key Insights
  - 🕐 Length of Membership is the strongest predictor of yearly spending.
  - 🤖 Linear Regression works as a solid baseline model.
