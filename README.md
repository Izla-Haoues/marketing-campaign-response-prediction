Marketing Campaign Response Prediction (Machine Learning)

This project builds a machine learning model that predicts which customers are likely to respond “yes” to a marketing campaign, using the well-known Bank Marketing Dataset (UCI).
It combines data analysis, feature engineering, and classification modeling to create a realistic, production-style marketing prediction pipeline.
The goal:
Help marketers target customers who are most likely to accept an offer, improving campaign efficiency and reducing cost.

Tech Stack
- Python
- Pandas, NumPy (data cleaning & preprocessing)
- Seaborn, Matplotlib (visualizations)
- Scikit-learn
       - Train/test split
       -  OneHotEncoder
       - StandardScaler
       - Logistic Regression
       - ColumnTransformer + Pipeline

Dataset Overview

The project uses the Bank Marketing Dataset from the UCI Machine Learning Repository.
Each row represents a customer contacted during a marketing campaign.

Key fields include:
- Demographics: age, job, marital, education
- Financial variables: balance, housing loan, personal loan
- Contact method: contact, day, month
- Call duration and campaign history: duration, campaign, pdays, previous
- Social & economic indicators: emp.var.rate, cons.price.idx, euribor3m, etc.
- Target variable: y → customer response (yes = 1, no = 0)

Machine Learning Approach

Preprocessing:
- Standardized numerical features
- One-hot encoded categorical features
- Built a unified ColumnTransformer + Pipeline

Model:
- Logistic Regression (max_iter=1000)
- Trained on 80% of the dataset
- Evaluated on held-out test data

Key Visualizations
These plots summarize model performance and customer insights.  

Confusion Matrix
Shows how well the model predicts responders vs non-responders.

Top Influential Features
Which characteristics most strongly increase or decrease the probability of response.

Response Rate by Job
Certain occupations are far more likely to accept marketing offers than others.

Response Rate by Age Group
Visualizing how likelihood of response changes across age ranges.

Project Workflow
1.Load & clean the dataset
2.Encode categorical variables
3.Scale numeric variables
4.Build ML pipeline
5.Train logistic regression model
6.Evaluate performance
7.Analyze feature importance
8.Generate marketing insights
9.Produce visualizations
10.Package results for GitHub

Insights & Interpretation
A few example trends this model reveals:
- Some job categories (e.g., student, retired) respond at much higher rates.
- Longer past call durations correlate strongly with a “yes.”
- Economic indicators influence campaign success.
- Certain age groups are consistently more receptive.
These insights allow marketers to target only high-probability customers, reducing costs and improving ROI.

Future Improvements
- Add Random Forest and XGBoost to compare performance
- Build a probability-based targeting dashboard
- Implement SHAP for deeper explainability
- Deploy the model as an API for real-time campaign scoring



   ## 📁 Project Files

```text
marketing_campaign_response_prediction.ipynb     # Full notebook
bank-full[1].csv                                 # Dataset
plots/
    confusion_matrix.png
    feature_importance.png
    response_by_job.png
    response_by_age_group.png


