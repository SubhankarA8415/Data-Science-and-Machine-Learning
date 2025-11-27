# 📊 Machine Learning & Data Science Projects

This repository showcases three well-structured ML & DS projects covering exploratory analysis, supervised learning, and production-level deployment.  
Each project demonstrates a different stage of a real-world ML workflow — from data exploration to fully hosted prediction APIs.

---

## 📁 Project Overview

### 1️⃣ **DataScience Project (End-to-End Data Analysis + ML Pipeline)**  
A complete exploratory ML workflow focused on understanding the dataset, transforming it, and training baseline models.

#### 🔍 Key Highlights
- Comprehensive **EDA**: correlation matrices, distribution analysis, outlier detection  
- Data preprocessing using:  
  - Missing value treatment  
  - Label/One-hot Encoding  
  - Feature Scaling  
- Built multiple models (Linear Regression, Decision Trees, etc.)  
- Compared model performance using:  
  - RMSE, MAE, R² Score  
- Visualized relationships using heatmaps, scatterplots, and pairplots  
- Documented insights and reasoning at each stage  
- Great introductory project showing understanding of ML workflow

🧪 **Environment:** Jupyter Notebook  
🚫 **No hosting / run only inside notebook**

---

### 2️⃣ **Supervised Learning – Capstone (Tree-Based Model Suite)**  
Focused entirely on powerful **tree-based algorithms** and model improvement techniques.

#### 🌳 Key Highlights
- Implemented **Decision Trees**, **Random Forest**, **Gradient Boosting**, **AdaBoost**, and **XGBoost**  
- Performed:
  - Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)  
  - Feature importance analysis  
  - Overfitting vs underfitting comparison  
- Visualization of decision boundaries and learning curves  
- Model evaluation using:  
  - Confusion Matrix  
  - Classification Report  
  - Accuracy, Precision, Recall, F1  
- Practical interpretation of ensemble behavior  
- Excellent for demonstrating depth in supervised learning techniques

🧪 **Environment:** Jupyter Notebook  
🚫 **No deployment / notebook execution only**

---

### 3️⃣ **Final ML Project – Random Forest Regressor (Hosted with Flask)**  
This is the production-ready ML project where the model is trained, saved, and deployed using an API endpoint.

#### 🚀 Key Highlights
- Built an optimized **Random Forest Regressor**  
- Models exported using `joblib`:  
  - `final_model.pkl`  
  - `col_names.pkl`  
- Created a **Flask REST API** that:  
  - Accepts JSON input  
  - Automatically aligns features using stored column names  
  - Returns predictions in JSON format  
- Designed endpoint `/predict` for real-time inference  
- Proper modular structure separating model, features, and API logic  
- Demonstrates practical ML deployment skills  

Below is a small snippet from `api.py` (full script in repo).  
📎 *Reference:* api.py logic extracted from uploaded file.

```python
@app.route('/predict', methods=['POST'])
def predict():
    df = pd.DataFrame(request.json)
    df = df.reindex(columns = col_names)
    prediction = list(model.predict(df))
    return jsonify({'prediction': str(prediction)})
```
---

## 📞 Contact

**Subhankar Pandit**  
**Full Stack Developer | Backend Engineer | AI/ML**  
**GitHub**: https://github.com/SubhankarA8415  
**LinkedIn**: https://linkedin.com/in/subhankar-pandit 
