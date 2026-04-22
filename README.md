
🏥 Medical Insurance Cost Prediction
Advanced Regression Analysis & Class Balancing
📌 Project Overview
This project focuses on predicting individual medical insurance charges by analyzing demographic and lifestyle data. The workflow moves from basic linear modeling to advanced ensemble techniques, with a specific emphasis on overcoming class imbalance and capturing non-linear interactions between health risks.

📊 Dataset & Feature Analysis
The study utilizes a dataset of 1,338 records, expanded to 2,128 through synthetic sampling.

Biological Factors: Age, BMI (Body Mass Index).

Categorical Factors: Sex, Smoking Status, Region, Number of Children.

Target Variable: charges (Total individual medical costs).

🛠️ Data Engineering Pipeline
I. Handling Imbalance (SMOTE)
The original dataset was heavily skewed toward non-smokers. To prevent the model from ignoring high-cost outliers, we implemented SMOTE (Synthetic Minority Over-sampling Technique).

Pre-SMOTE: ~20% Smoker representation.

Post-SMOTE: 50/50 Balanced representation (Total rows: 2,128).

II. Categorical Encoding & Scaling
We utilized One-Hot Encoding for categorical features and StandardScaler to normalize numerical inputs, ensuring that distance-based models like KNN and high-variance models like Random Forest perform optimally.

III. Capturing Interaction Terms
Applied PolynomialFeatures (Degree 2) to model the synergistic effects between variables, such as the compounding cost of being both a smoker and having a high BMI.

🔬 Model Evaluation & Results
We benchmarked several algorithms using 10-fold Cross-Validation to ensure generalizability:

Model Architecture	R² Score (Avg)	Status
Linear Regression	0.820	Baseline
Polynomial Regression	0.892	Non-Linear Fit
Random Forest (Tuned)	0.925	Optimal Model
💡 Key Business Insights
The "Smoker Multiplier": Smoking is the primary driver of insurance cost. However, the model revealed that the cost for smokers increases exponentially when combined with a high BMI, rather than linearly.

Demographic Neutrality: Factors such as Sex and Region had negligible predictive power, suggesting that premiums are predominantly risk-based rather than geographic or gender-based.

Ensemble Advantage: The transition from a 0.82 to 0.92 R² score highlights that tree-based ensembles are far superior for insurance data due to their ability to handle the "stratified bands" of costs seen in the EDA.

💻 Tech Stack
Data Science: Python, Pandas, NumPy

Machine Learning: Scikit-Learn, Imbalanced-Learn (SMOTE)

Visualization: Matplotlib, Seaborn

🏁 Final Conclusion
By evolving the model through SMOTE and Hyperparameter Tuning via GridSearchCV, we achieved a high-stability model capable of explaining 92.5% of the variance in insurance charges. This tool provides a robust framework for automated risk assessment and premium estimation.
