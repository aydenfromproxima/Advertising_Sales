# Advertising Data Analytics – Sales Prediction Using Machine Learning

A complete machine learning project built to analyze advertising spend across TV, Radio, and Newspaper channels, and predict Sales using multiple regression models.

---

## Dataset Overview

The dataset contains **200 advertising records** with the following features:

- TV  
- Radio  
- Newspaper  
- Sales (Target)  

### Key Details

- No missing values in the dataset  
- Two outliers detected in the **Newspaper** column using the IQR method and removed  
- Final dataset used for modeling: **198 rows × 4 columns**

---

## Data Preparation

Steps performed:

- Loaded CSV and verified shape (**200 × 4**)  
- Confirmed **0 missing values**  
- Verified no duplicate entries  
- Visualized distributions using boxplots  
- Identified and removed outliers (IQR)  
- Split dataset into training/testing (**70% / 30%**)  
- Applied **StandardScaler** for feature normalization  
- Separated feature variables (TV, Radio, Newspaper) and target (Sales)

---

## Analysis & Visualizations

### 1. Data Distribution
- Boxplots showed wide variance in TV spending  
- Newspaper included mild outliers  
- TV, Radio, and Sales showed no outliers

### 2. Outlier Detection
- Only the Newspaper column contained **2 meaningful outliers**

### 3. Train–Test Split
- Training samples: **138**  
- Testing samples: **60**

### 4. Feature Scaling
- Standardization significantly improved model stability and accuracy  

---

## Machine Learning Models

Models trained after cleaning, scaling, and splitting:

### Linear Regression
- MAE: 1.18  
- RMSE: 1.58  
- Accuracy: **91.39%**

### Decision Tree Regression
- MAE: 1.04  
- RMSE: 1.53  
- Accuracy: **91.75%**

### Random Forest Regression
- MAE: 0.93  
- RMSE: 1.15  
- Accuracy: **93.40%**

### XGBoost Regression
- MAE: 0.86  
- RMSE: 1.17  
- Accuracy: **93.90%**

### Cross-Validation Scores

| Model             | Mean CV Accuracy |
|------------------|------------------|
| Linear Regression | 0.897            |
| Decision Tree     | 0.853            |
| Random Forest     | 0.927            |
| XGBoost           | **0.934** (best) |

---

## Final Model

- **XGBoost Regressor** selected as final model  
- StandardScaler used for feature normalization  
- Model exported as `hr.pkl`  
- Scaler exported as `schr.pkl`  

---

## Deployment

The project includes two user interfaces:

- Tkinter Desktop Application  
- Streamlit Web Application  

---

## Key Insights

- TV and Radio advertising have the strongest positive impact on Sales  
- Newspaper spending provides weak predictive power, especially after outlier removal  
- Random Forest and XGBoost achieved high accuracy (~94%)  
- Feature scaling improved model consistency  
- Higher TV advertising budgets consistently correlate with higher sales  

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Seaborn  
- Matplotlib  
- Tkinter  
- Streamlit  

---

## How to Run the Project

### 1. Clone the Repository
` ` `bash git clone https://github.com/yourusername/AdvertisingSalesPrediction.git

### 2. Install Dependencies
bash

Copy code

pip install pandas numpy matplotlib seaborn scikit-learn xgboost streamlit
### 3. Run the Notebook
bash

Copy code

jupyter notebook Advertising_Sales_Prediction.ipynb
### 4. Launch the Streamlit App
bash

Copy code

streamlit run hrapp.py

---

## Future Improvements
- Add SHAP explainability for model interpretation

- Build an interactive dashboard (Streamlit or PowerBI)

- Perform hyperparameter tuning for each model

- Add advanced feature importance visualizations

- Deploy as a complete web application

---

## Contributing
Pull requests are welcome.

You may enhance models, add visualizations, or extend deployment workflows.

---

## Support
If you found this project useful, consider starring the repository.
