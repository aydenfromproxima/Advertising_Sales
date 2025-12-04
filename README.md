# Advertising Data Analytics – Sales Prediction Using Machine Learning

**Dataset Overview**

The dataset contains 200 advertising records with 4 features:

TV

Radio

Newspaper

Sales (Target)

Key Details

No missing values were found in the dataset 

Two outliers were detected in the Newspaper column using the IQR method and removed before modeling (Page 4 boxplot & code) 

Final dataset used for modeling: 198 rows × 4 columns.

**Data Preparation**

In the notebook, I:

Loaded CSV and confirmed dataset shape → 200 × 4 

0c704773-f191-4604-b4c9-cfe2a6c…

Checked missing values → 0 missing values

Checked duplicates → No duplicates

Visualized distributions using boxplots (Page 4)

Identified and removed outliers using IQR

Split data into training/testing → 70% / 30%

Normalized features using StandardScaler

Prepared features (TV, Radio, Newspaper) and target (Sales)

**Analysis & Visualizations**

The project includes several analyses and plots:

1. Data Distribution

Boxplots revealed wide variance in TV spend and mild outliers in Newspaper (Page 4 image) 

0c704773-f191-4604-b4c9-cfe2a6c…

2. Outlier Detection

Newspaper had 2 outliers

TV, Radio, Sales had no outliers

3. Train-Test Split

Training samples → 138
Testing samples → 60

4. Feature Scaling

StandardScaler was applied to improve model performance (Page 10 code snippet).

**Machine Learning Models**

The following ML models were trained after cleaning, normalization, and splitting:

_Linear Regression_

MAE: 1.18

RMSE: 1.58

Accuracy: 91.39% (based on 1 - MAPE)
(Results on Page 15) 

_Decision Tree Regression_

MAE: 1.04

RMSE: 1.53

Accuracy: 91.75%
(Page 16) 

_Random Forest Regression_

MAE: 0.93

RMSE: 1.15

Accuracy: 93.40%
(Page 16) 

_XGBoost Regression_

MAE: 0.86

RMSE: 1.17

Accuracy: 93.90%
(Page 17) 


Cross Validation
Model	Mean CV Accuracy
Linear Regression	0.897
Decision Tree	0.853
Random Forest	0.927
XGBoost	0.934 (best)

(Page 17–18) 

**Final Model**

XGBoost Regressor selected as final model

StandardScaler used for feature normalization

Exported model as hr.pkl

Exported scaler as schr.pkl
(Page 18–19) 

**Deployment**

Project includes two interfaces:

Tkinter Desktop App (Page 19 code)

Streamlit Web App (Page 20 code)

**Key Insights**

TV and Radio advertising strongly influence Sales

Newspaper has weak predictive power, especially after outlier removal

XGBoost and Random Forest gave high predictive accuracy (~94%)

Feature scaling significantly improved model stability

Ads with high TV budget consistently generated higher sales

**Languages & Libraries Used**

Python
Pandas
NumPy
Scikit-learn
XGBoost
Seaborn
Matplotlib
Tkinter
Streamlit

How to Run the Project
1. Clone the Repository
git clone https://github.com/yourusername/AdvertisingSalesPrediction.git

2. Install Dependencies
pip install pandas numpy matplotlib seaborn scikit-learn xgboost streamlit

3. Run the Notebook
jupyter notebook Advertising_Sales_Prediction.ipynb

4. Run Streamlit App
streamlit run hrapp.py

Future Improvements

Add SHAP explainability for model interpretation

Build an interactive dashboard (Streamlit/PowerBI)

Add hyperparameter tuning for each model

Include feature importance visualizations

Deploy as a full web application

Contributing

Pull requests are welcome.
You can improve models, add visualizations, or extend deployment.

**If You Found This Useful:**

Star the repository to support more data analytics projects!
