### Project Title
**Predicting High-Value Customers in Online Retail Using Machine Learning**

#### Author
An Tian

#### Abstract
This project developed a Random Forest classifier to identify high-value customers from transaction data, achieving 0.98 AUC. Key findings show transaction frequency and product diversity are top predictors. The model enables targeted marketing strategies to improve customer retention and revenue.

#### Rationale
Identifying high-value customers allows businesses to:
- Optimize marketing spend
- Improve customer retention
- Increase lifetime value
- Enhance strategic decision-making

#### Research Question
Can we accurately predict high-value customers (top 50% spenders) based on their transaction patterns?

#### Data Sources
- Primary: UCI Online Retail Dataset (541,909 transactions)
- Fallback: Synthetic data generator (used if network fails)

#### Methodology
1. **Data Processing**:
   - Removed canceled orders
   - Created temporal features (hour/day/month)
   - Generated 10 customer-level aggregate features

2. **Modeling**:
   - Random Forest with SMOTE for class imbalance
   - 80/20 stratified train-test split
   - Hyperparameters: 100 trees, max_depth=8

3. **Evaluation Metrics**:
   - AUC-ROC, F1-score, Precision-Recall

#### Results
- **Accuracy**: 85%  
- **Key Predictors**:  
  1. Transaction count (28% importance)  
  2. Active months (19%)  
  3. Unique products purchased (15%)  

#### Next steps
1. Test alternative models (XGBoost, Neural Networks)
2. Incorporate external demographic data
3. Develop real-time prediction API
4. Implement model monitoring system

#### Conclusion
The model successfully identifies high-value customers with strong accuracy (AUC 0.98). Key recommendations include focusing retention efforts on frequent buyers and optimizing marketing timing based on shopping patterns. Future work should expand feature engineering and model testing.

### Bibliography
1. Chen, T., & Guestrin, C. (2016). "XGBoost". ACM SIGKDD.  
2. Breiman, L. (2001). "Random Forests". Machine Learning 45(1).  
3. UCI Machine Learning Repository. (2015). "Online Retail Dataset".  

##### Contact and Further Information
Email: [atian2@hawk.iit.edu]  