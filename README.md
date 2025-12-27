# Bank Marketing Campaign Analysis: Classifier Performance Comparison

## Project Overview
This project aims to optimize telemarketing campaigns for a Portuguese banking institution. By leveraging machine learning, we identify which customers are most likely to subscribe to a term deposit. This allows the bank to focus its resources on high-potential leads, improving conversion rates and reducing operational costs.

## Business Problem
The bank conducts phone-based marketing. The goal is to predict the success of these calls (target variable `y`: 'yes' or 'no'). 
- **Challenge**: The dataset is highly imbalanced (~89% 'no').
- **Constraint**: The 'duration' feature is excluded from modeling to ensure the results are predictive for future calls, as the duration is only known after the call is finished.

## Dataset
- **Source**: UCI Machine Learning Repository (Bank Marketing Dataset).
- **Size**: 41,188 entries with 21 attributes.
- **Features**: Demographics (age, job, marital), social-economic indicators (euribor3m, nr.employed), and campaign history.

## Methodology
1. **Data Cleaning & Engineering**: 
   - Handled categorical variables using One-Hot Encoding.
   - Scaled numerical features using StandardScaler.
   - Removed 'duration' to prevent data leakage.
2. **Baseline**: Established a baseline accuracy of **88.74%** (predicting the majority class).
3. **Classifiers Tested**:
   - Logistic Regression
   - K-Nearest Neighbors (KNN)
   - Decision Trees
   - Support Vector Machines (SVM)
4. **Evaluation**: Used Accuracy, Precision, Recall, and F1-Score to compare performance.

## Key Findings
| Model | Accuracy |  
| :--- | :--- |
| **Baseline** | 88.74%  |
| **Logistic Regression** | 90.14%  |
| **KNN** | 89.49% |
| **Decision Tree** | 90.11% |
| **SVM** | 90.24%  |

### Actionable Insights:
- **Economic Sensitivity**: Economic indicators like `nr.employed` and `euribor3m` are the strongest predictors. Campaigns should be timed based on these macroeconomic trends.
- **Segment Targeting**: Retirees and students show higher conversion rates.
- **Recency Matters**: Clients contacted recently in previous campaigns are significantly more likely to subscribe.

## Files in this Repository
- `bank_marketing_analysis.ipynb`: The primary Jupyter Notebook with code, plots, and detailed analysis.
- `model_performance_results.csv`: A summary table of the performance metrics for all models.
- `bank-additional-full.csv`: The raw dataset used for the analysis.
- `README.md`: Project documentation.

## How to Run
1. Ensure you have Python 3.x and the following libraries installed: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`.
2. Place the `bank-additional-full.csv` file in the same directory as the notebook.
3. Open and run the `bank_marketing_analysis.ipynb` file.
