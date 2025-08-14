# Customer Churn Analysis: Predictive Modeling for Retention Strategy

An end-to-end capstone project using interpretable machine learning and interactive dashboards to identify key drivers of churn and power proactive retention in subscription-based telecom services.

---

## 🚀 Project Overview

Subscription businesses spend up to 5× more to acquire a new customer than to retain an existing one. This project turns churn prediction from a reactive challenge into a strategic advantage by:

- Diagnosing the root causes of churn across demographics, service usage, and payment behaviors  
- Building two complementary models (Logistic Regression, Decision Tree) with clear business-ready outputs  
- Packaging insights into an interactive Tableau dashboard for real-time risk monitoring  

Key impact metrics:

- Logistic Regression AUC: **0.836**, Recall: **91.0%**  
- Contract terms drive **80%** of predictive power  
- Month-to-month fiber customers on electronic checks churn at **45–50%**  

---

## 📊 Problem Statement & Business Context

Subscription churn silently erodes revenue. Traditional retention tactics often:

- Over-spend on low-risk groups  
- Overlook high-risk segments  
- React to cancellations instead of preventing them  

A data-driven approach can recover millions in revenue by shifting to proactive, targeted retention campaigns.

---

## 📈 Data Overview & Methodology

Dataset: Telco Customer Churn (Kaggle)  
- 7,043 customer records, 21 features  
- Demographics, services (internet, streaming), account info (contracts, payments), financials (tenure, charges)  

Workflow:

1. Data cleaning & feature engineering (tenure buckets, dummy encoding)  
2. Exploratory Data Analysis (family ties, age, payment methods, tenure pricing paradox)  
3. Model development (Logistic Regression for interpretability, Decision Tree for non-linear insights)  
4. Performance evaluation focused on business metrics (AUC, recall, precision)  
5. Insight packaging via interactive Tableau dashboard  

Tools & Tech: Python (Pandas, NumPy, Scikit-learn), Matplotlib, Seaborn, Tableau Public  

---

## 🔍 Key Findings: Customer Behavior

- **Family Structure**  
  - No partner/no dependents churn at **34.2%**  
  - Partner + dependents churn at **14.2%**  
- **Age**  
  - Seniors churn at **42%** vs **24%** for non-seniors  
- **Payment Method**  
  - Electronic checks: **45.3%** churn  
  - Automatic payments: **15–17%** churn  
- **Tenure & Pricing**  
  - Loyal customers pay more: \$56.17/mo (0–12 mo) → \$75.95/mo (61+ mo)  
- **Contract Terms**  
  - Month-to-month: **31.5–48.3%** churn  
  - One-year: **7.1–14.8%** churn  
  - Two-year: **1.6–4.2%** churn  
- **Paperless Billing Paradox**  
  - Paperless users churn **1.5×** more than paper statement users  
- **Service Quality Flag**  
  - Fiber internet customers churn disproportionately, signaling quality or expectation gaps  

---

## 🤖 Predictive Modeling & Performance

| Model                 | AUC   | Precision | Recall  | Accuracy |
|-----------------------|-------|-----------|---------|----------|
| Logistic Regression   | 0.836 | 0.504     | 0.910   | 0.739    |
| Decision Tree         | 0.798 | 0.426     | 0.929   | 0.653    |

- Logistic Regression offers clear coefficient insights and risk-tier scoring  
- Decision Tree excels at recall but incurs more false positives  

### Feature Importance (Logistic Regression)

| Feature               | Importance (%) |
|-----------------------|----------------|
| Two-year contract     | 49.2           |
| One-year contract     | 30.8           |
| Fiber internet        | 13.5           |
| Streaming movies      | 4.1            |
| Total charges         | 1.2            |

---

## 📊 Interactive Dashboard

A Tableau Public dashboard allows dynamic filtering by churn score, tenure, contract, and payment to:

- Identify the highest-risk cohort: month-to-month fiber customers on e-checks (< 12 mo tenure)  
- Drill into senior, family-tie, and paperless billing segments  

PDF export included for quick sharing.

---

## 💡 Business Recommendations

### Immediate (0–3 Months)

1. **Contract Incentive Program**  
   - 10–15% discount for one-year, 15–20% for two-year commitments  
   - Add perks: free install, equipment upgrades, premium support  

2. **Payment Method Migration**  
   - \$5–10/mo bill credit + one-time signup bonus for auto-pay  
   - Guided enrollment to remove friction  

3. **Predictive Scoring Deployment**  
   - Integrate LR model into CRM for real-time churn risk scores  
   - Trigger tiered outreach based on individual risk  

### Strategic (3–12 Months)

- **Fiber Service Quality Initiative**: targeted surveys, ticket analysis, infrastructure upgrades  
- **Senior Citizen Program**: dedicated support, simplified packages, family plan incentives  

---

## 🎯 Success Metrics & KPIs

| Metric                        | Baseline    | 6-month Target | 12-month Target |
|-------------------------------|-------------|----------------|-----------------|
| Overall Churn Rate            | ~27%        | < 22%          | < 20%           |
| Month-to-Month Churn          | > 40%       | < 30%          | < 25%           |
| Electronic Check Churn        | 45.3%       | < 30%          | < 25%           |
| Contract Conversion Rate      | —           | 15%            | 25%             |
| Payment Method Migration Rate | —           | 20%            | 35%             |

---

## 🔮 Future Research Directions

- Ensemble models (Random Forest, Gradient Boosting, Neural Nets)  
- Time series analysis for seasonality effects  
- Customer Lifetime Value–weighted modeling  
- Integration of support tickets, usage logs, competitive data  
- A/B testing framework for optimizing incentives and interventions

---
# 📊 Interactive Dashboard
Explore the interactive Tableau dashboard for dynamic analysis:
- 🔗 Customer Churn Analysis Dashboard (https://public.tableau.com/app/profile/shayma.remy/viz/CustomerChurnAnalysis_17541038065910/CoverPage)
# Dashboard Features
- Dynamic filtering by risk scores, tenure, and contract types
- Interactive segment identification
- Real-time drill-down capabilities
- Business intelligence insights

## 📂 Notebooks & Report

- **1_Data_Wrangling.ipynb** – cleans raw CSV, encodes categorical variables, derives tenure buckets  
- **2_EDA.ipynb** – demographic, service, and payment behavior analyses with Matplotlib & Seaborn  
- **3_Modeling.ipynb** – trains models, evaluates confusion matrices, ROC curves, and feature importances  
- **Capstone_Final_Report.pdf** – narrative report with executive summary, visuals, and business recommendations  
- **Customer_Churn_Analysis_Predictive_Modeling_for_Retention_Strategy.pdf** – Notion-exported project overview with extended insights


You can view them directly on GitHub:
- Churn_Prediction_for_Online_Subscription_Services_Data_Wrangling.ipynb – https://github.com/Shaymaxo/Capstone-3-Springboard/blob/main/Churn_Prediction_for_Online_Subscription_Services_Data_Wrangling.ipynb
- Churn_Prediction_for_Online_Subscription_Services_EDA.ipynb – https://github.com/Shaymaxo/Capstone-3-Springboard/blob/main/Churn_Prediction_for_Online_Subscription_Services_EDA.ipynb
- Churn_Prediction_for_Online_Subscriptions_Modeling.ipynb – https://github.com/Shaymaxo/Capstone-3-Springboard/blob/main/Churn_Prediction_for_Online_Subscriptions_Modeling.ipynb
- Capstone_Final_Report.pdf – https://github.com/Shaymaxo/Capstone-3-Springboard/blob/main/report/Capstone_Final_Report.pdf
- Customer_Churn_Analysis_Predictive_Modeling_for_Retention_Strategy.pdf – https://github.com/Shaymaxo/Capstone-3-Springboard/blob/main/report/Customer_Churn_Analysis_Predictive_Modeling_for_Retention_Strategy.pdf

---

## ⚙️ Setup & Dependencies

1. Clone this repository  
   ```bash
   git clone https://github.com/Shaymaxo/Capstone-3-Springboard.git
   cd Capstone-3-Springboard
2. (Optional) Create and activate a virtual environment
   ```bash
    python3 -m venv venv
   source venv/bin/activate
3. Install required Python packages
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn notebook
4. Launch Jupyter Notebook
   ```bash
    jupyter notebook notebooks/

📈 Model Metrics
A concise summary of the final models’ features, parameters, and performance is provided in model_metrics.csv.

⭐ How to Cite / Acknowledge
If you use this project for learning or production guidance, please reference the Springboard Data Science Career Track Capstone.

🤝 Questions & Feedback
For any questions or suggestions, open an issue or reach out to Shayma on GitHub. Happy analyzing!

# Acknowledgments
- Kaggle for providing the Telco Customer Churn dataset
- Springboard for capstone project guidance
- Tableau Public for dashboard hosting capabilities

# 📚 References & Resources
- Dataset Source: Kaggle - Telco Customer Churn (https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Business Context: Customer retention economics in subscription businesses
- Technical Implementation: Scikit-learn documentation and best practices
- Visualization: Tableau Public dashboard development


This project demonstrates the application of data science techniques to solve real-world business problems through predictive modeling and actionable insights for customer retention strategy.

# 🎯 Project Highlights
- ✅ Data Science Excellence: Complete ML pipeline from EDA to deployment
- ✅ Business Impact: Clear ROI through targeted retention strategies
- ✅ Model Interpretability: Explainable AI for stakeholder confidence
- ✅ Interactive Visualization: Professional dashboard for ongoing analysis
- ✅ Production Ready: Scalable implementation for business integration

⭐ Star this repository if you found it helpful!
