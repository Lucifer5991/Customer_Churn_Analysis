A comprehensive end‑to‑end predictive analytics project focused on understanding and forecasting customer churn for a subscription‑based digital services company. This project covers the full data science workflow, from data cleaning and feature engineering to outlier treatment, exploratory analysis, and machine learning model development.

PROJECT OVERVIEW
Customer churn is a critical challenge for subscription‑driven businesses. Retaining customers is significantly more cost‑effective than acquiring new ones, making churn prediction an essential analytical capability.
This project applies predictive analytics techniques to a large customer dataset (50,000 records, 35 features) to:
• 	Identify key drivers of churn
• 	Build machine learning models to predict churn
• 	Provide actionable insights to support customer retention strategies
The analysis integrates demographic, behavioral, financial, and service‑related attributes to uncover patterns that influence customer attrition.

DATASET SUMMARY

The dataset includes:
• Demographic Features
  Age, Gender, Income Tier, Education, Region, Tier, Customer Segment
• Subscription & Contract Details
  ContractLength, PlanType, TenureMonths, PaymentMethod, AutoPay, Paperless,         ContractAutoRenew
• Behavioural & Usage Metrics
MonthlyCharges, TotalCharges, LoginsLastMonth, UsageChangePct, RFMScore, CompetitorIndex 
• Service Experience
  TicketsOpened, TicketsResolutionTime, SupportChannelPreferred, ComplaintCategory
• Acquisition & Device Information
  ReferralSource, ChannelPreferred, DeviceType, DeviceOS
  Target Variable:
  (0 = No, 1 = Yes)

EXPLORATORY DATA ANALYSIS (EDA)

Key findings from the EDA:
• 	Class imbalance: Majority of customers did not churn
• 	Outliers: Extreme values in Age, TenureMonths, MonthlyCharges, TotalCharges
• 	Categorical inconsistencies: Variants like “Basic”, “basic” and “Basik”
•      Complaint Category Imbalance: Technical issues dominate
• 	Weak linear correlations: Numerical variables show limited direct correlation with churn
Visualizations included:
• 	Histograms
• 	Boxplots
• 	Bar charts
• 	Correlation heatmap

Data Cleaning & Feature Engineering
• Missing Values
Handled using mean/median imputation for numerical fields.
•  Categorical Standardization
Converted inconsistent labels to lowercase and unified formats.
• Data Type Corrections
Ensured numerical fields were properly typed.
• Duplicate Removal
Eliminated redundant records.
•  Feature Engineering
Created new derived metrics such as average monthly charges and interaction features.
• Encoding
- Binary variables → 0/1
- Multi-category variables → One-hot encoding

 OUTLIER DETECTION & TREATMENT 
A combination of:
•  IQR Method
Used for skewed variables such as:
- TenureMonths
- MonthlyCharges
- TotalCharges
- UsageChangePct
- CompetitorIndex
•   Business Rule Validation
Removed:
- TenureMonths = 0
- CompetitorIndex > 1
- Unrealistic usage spikes
- Invalid billing values
•   Results
- 567 rows removed (1.13%)
- Distribution shapes preserved
- Improved model stability

 PREDICTIVE MODELLING 
Multiple machine learning models were developed and evaluated:
Models Implemented
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- Support Vector Machine (SVM)
- Artificial Neural Network (MLPClassifier)
Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
Key Observations
- Logistic Regression provided a strong baseline but struggled with nonlinear patterns
- Decision Trees captured interactions but risked overfitting
- Ensemble models (Random Forest, Gradient Boosting, XGBoost) delivered superior performance
- Neural networks performed well but required careful tuning

 RESULTS & INSIGHTS 
- TenureMonths showed a modest negative correlation with churn, newer customers are more likely to leave
- Technical complaints were a major churn driver
- Billing and usage anomalies strongly influenced churn likelihood
- Ensemble models achieved the best predictive performance
- Outlier removal significantly improved model stability
These insights can support targeted retention strategies such as:
- Early engagement programs for new customers
- Proactive technical support
- Billing transparency improvements

 TECH STACK 
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook


 CONCLUSION
This project demonstrates a complete predictive analytics workflow applied to a real-world churn problem. Through rigorous data cleaning, feature engineering, outlier treatment, and model comparison, it provides actionable insights and a strong predictive foundation for customer retention strategies.


