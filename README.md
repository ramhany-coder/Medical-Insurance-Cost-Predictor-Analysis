# Medical Insurance Cost Prediction

This project aims to accurately predict individual medical insurance charges based on demographic and lifestyle data. By exploring various regression techniques, the project identifies the key drivers of insurance costs and demonstrates the importance of modeling non-linear relationships in healthcare data.

## 📊 Dataset Analysis
The analysis is performed on a dataset containing 1,338 records with the following features:
* **Demographics:** Age, Sex, Children (number of dependents), and Region.
* **Lifestyle:** BMI (Body Mass Index) and Smoking Status.
* **Target:** Charges (Individual medical costs billed by health insurance).

## 🚀 Key Features
* **Exploratory Data Analysis (EDA):** Visualizing correlations, with a heavy focus on the impact of smoking and BMI on costs.
* **Feature Engineering:** Implementation of `PolynomialFeatures` to capture complex interactions between variables.
* **Model Comparison:** * **Linear Regression:** Established a baseline R² score (approx. 0.78).
    * **Polynomial Regression:** Improved performance by modeling non-linear trends.
    * **Random Forest Regressor:** Achieved the highest accuracy (approx. 0.847) through ensemble learning.
* **Hyperparameter Tuning:** Utilized `GridSearchCV` and 5-fold Cross-Validation to optimize model performance and ensure generalizability.

## 📈 Key Insights
* **Non-Linearity:** The significant jump in accuracy from Linear to Random Forest models proves that interactions—specifically between BMI and Smoking status—are the primary drivers of insurance costs.
* **Feature Importance:** Lifestyle (Smoking) and Age are the most influential variables, whereas Region and Sex show minimal impact on final charges.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Handling:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-learn

## 📂 Repository Structure
* `insurance.ipynb`: Complete Jupyter Notebook with data cleaning, EDA, and model training.
* `insurance.csv`: (Optional: Add link to dataset or upload file).

## 📝 Conclusion
The project concludes that while linear models provide a solid baseline, ensemble methods like Random Forest are superior for healthcare cost prediction due to their ability to capture the synergistic effects of risk factors like high BMI combined with smoking.
