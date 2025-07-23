# online-purchase-prediction

# 🛒 Online Purchase Prediction using Logistic Regression

This machine learning project aims to predict whether a customer will make a purchase based on their behavior and interaction with an online store. The prediction helps businesses to better target customers and optimize their marketing strategies.

---

## 🎯 Project Objective

To build a classification model using **Logistic Regression** that can accurately predict customer purchase behavior using browsing activity and previous purchase history.

---

## 📂 Dataset Overview

The dataset contains the following features:

- **User ID** – Unique customer identifier  
- **Time Spent on Site** – Duration spent on the website (in minutes)  
- **Page Views** – Number of product or page views  
- **Ad Clicked** – Whether the user clicked an ad (1 = Yes, 0 = No)  
- **Device Type** – Type of device used (Mobile/Desktop)  
- **Previous Purchases** – Number of purchases previously made  
- **Made Purchase** – Target variable (1 = Purchase, 0 = No Purchase)

> File used: `online purchase prediction.csv`

---

## 🛠️ Technologies Used

- **Programming Language**: Python  
- **Tools**: Jupyter Notebook  
- **Libraries**:  
  - `pandas`, `numpy` for data handling  
  - `matplotlib`, `seaborn` for visualization  
  - `scikit-learn` for model training and evaluation  
  - `joblib` to save/load models

---

## 🔁 Workflow Summary

1. **Data Preprocessing**
   - Label encoding for categorical columns (like Device Type)
   - Train-test split

2. **Exploratory Data Analysis (EDA)**
   - Visualizations to analyze user behavior and its impact on purchases

3. **Model Building**
   - Logistic Regression model trained on preprocessed data

4. **Model Evaluation**
   - Confusion matrix and accuracy score

5. **Model Export**
   - Final model saved as `madepurchase.pkl`

---

## 📊 Model Evaluation

- **Model Used**: Logistic Regression  
- **Output**:  
  - `1` = Made a purchase  
  - `0` = Did not purchase  
- **Accuracy**: *[Add final accuracy here]*

---

## 📁 Project Structure

```
├── ML Project.ipynb                # Jupyter Notebook file
├── online purchase prediction.csv  # Dataset file
├── madepurchase.pkl                # Trained ML model
└── README.md                       # Project documentation
```

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/online-purchase-prediction.git
   cd online-purchase-prediction
   ```

2. Open and run the notebook:
   - File: `ML Project.ipynb`

3. Load the trained model:
   ```python
   import joblib
   model = joblib.load('madepurchase.pkl')
   ```

4. Make a prediction:
   ```python
   # Example: [TimeSpent, PageViews, AdClicked, DeviceType, PrevPurchases]
   input_data = [[12.5, 10, 1, 0, 2]]  # Assume 0 = Desktop, 1 = Mobile after encoding
   result = model.predict(input_data)
   print("Prediction:", result)
   ```

---

## 🔮 Future Enhancements

- Add new features (e.g., session time, referral source)
- Try different models (Random Forest, XGBoost)
- Build a web dashboard using Streamlit
- Deploy model as a REST API
