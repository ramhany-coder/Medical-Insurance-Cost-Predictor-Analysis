🏥 Medical Insurance Cost Prediction
This project develops a high-precision predictive model for individual medical insurance charges. By leveraging demographic and lifestyle data, we move from simple linear baselines to advanced ensemble methods, specifically addressing data imbalance and non-linear interactions.

📊 Dataset Overview
The analysis is performed on a dataset containing 1,338 original records with the following features:

Demographics: Age, Sex, Children, and Region.

Health/Lifestyle: BMI (Body Mass Index) and Smoking Status.

Target: charges (Continuous numerical value).

🚀 Key Technical Milestones
1. Data Re-balancing (SMOTE)
Our EDA identified a significant minority of smokers (~20%). We implemented SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset to 2,128 records, ensuring the model accurately learns the "high-cost" smoking patterns without bias.

2. Feature Engineering & Pipelines
Encoding: Full One-Hot Encoding for categorical variables.

Polynomial Expansion: Generated interaction terms (e.g., Age×BMI) to capture non-linear compounding risks.

Standardization: Applied StandardScaler within a Pipeline to prevent data leakage during cross-validation.

3. Model Evolution
We compared three distinct modeling approaches:

Model	Strategy	R² Score
Linear Regression	Baseline	0.82
Polynomial Reg.	Capture Interactions	0.89
Random Forest	Optimized Ensemble	0.925
📈 Key Insights
Synergistic Risks: The interaction between BMI and Smoking is the single largest driver of extreme insurance costs.

Stability: Through 10-fold Cross-Validation and GridSearchCV, the Random Forest model demonstrated high stability, maintaining accuracy across different data subsets.

Impact Drivers: Lifestyle (Smoking) and Age are high-impact variables, while geographical Region and Sex have minimal influence on final premiums.

🛠️ Tech Stack
Core: Python, Pandas, NumPy.

Visualization: Seaborn, Matplotlib.

ML Library: Scikit-learn, Imbalanced-learn (for SMOTE).

📂 Repository Structure
insurance.ipynb: Full research notebook including EDA, SMOTE implementation, and Hyperparameter tuning.

insurance.csv: The raw dataset used for training and testing.

📝 Final Conclusion
The project concludes that while linear models provide a solid baseline, ensemble methods like Random Forest are superior for healthcare cost prediction. By specifically addressing class imbalance and feature interactions, we achieved a final R² score of 0.925, providing a robust tool for risk assessment.
