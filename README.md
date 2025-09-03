
# HR Attrition Prediction using sklearn

## Project Overview
This project predicts employee attrition using machine learning models (Decision Tree & Random Forest) on HR datasets. It provides data-driven insights to help HR proactively identify employees at risk of leaving, based on factors like satisfaction, tenure, workload, and performance.

---

## Dataset
- **Source:** Internal HR dataset  
- **Records:** 1,200+ employees  
- **Features:** satisfaction_level, last_evaluation, number_project, average_monthly_hours, tenure, work_accident, promotion_last_5years, department, salary  
- **Target:** left (1 if employee left, 0 otherwise)

---

## Models and Results

### Decision Tree
| Model             | Precision | Recall   | F1       | Accuracy  | AUC      |
|------------------|-----------|----------|----------|----------|----------|
| Decision Tree CV  | 0.9146    | 0.9169   | 0.9157   | 0.97198  | 0.96982  |
| Decision Tree2 CV | 0.9146    | 0.9169   | 0.9157   | 0.97198  | 0.96982  |

**Accuracy & AUC**
- Tree1 Accuracy: 0.97198, AUC: 0.96982  
- Tree2 Accuracy: 0.97198, AUC: 0.96982  

---

### Random Forest
| Model             | Precision | Recall   | F1       | Accuracy  | AUC      |
|------------------|-----------|----------|----------|----------|----------|
| Random Forest CV  | 0.9876    | 0.9103   | 0.9473   | 0.9832   | 0.9803   |
| Random Forest2 CV | 0.9500    | 0.9156   | 0.9325   | 0.9780   | 0.9804   |
| Random Forest2 Test | 0.9642  | 0.9197   | 0.9414   | 0.9810   | 0.9564   |

**Accuracy & AUC**
- RF1 Accuracy: 0.98321, AUC: 0.98032  
- RF2 Accuracy (CV): 0.97798, AUC: 0.98042  
- RF2 Accuracy (Test): 0.98099, AUC: 0.95644  

---

## Key Insights
- Models show high predictive accuracy (>97% for trees, >98% for RF).  
- Random Forest improves over Decision Tree by 1–2% in accuracy.  
- AUC values indicate strong separability between employees who leave and stay.

---

## HR Recommendations
1. Boost employee satisfaction via surveys, rewards, and growth opportunities.  
2. Manage workload: distribute projects evenly, set realistic deadlines, and encourage breaks.  
3. Retain shorter-tenured employees with career plans, mentorship, and stay interviews.  
4. Promote work-life balance: flexible schedules, wellness programs, discourage overtime.  
5. Use predictive models to identify at-risk employees proactively.

---

## Tools & Libraries
- Python 3  
- **sklearn**: Decision Tree, Random Forest, GridSearchCV  
- Pandas, NumPy, Matplotlib, Seaborn  
- Pickle for model saving and loading  

---

## How to Use
1. Clone the repository  
2. Load dataset: `df = pd.read_csv("HR_capstone_dataset.csv")`  
3. Run preprocessing and feature engineering steps  
4. Train models with GridSearchCV or load saved models using pickle  
5. Evaluate models and compare accuracy & AUC  

---

## Saved Models
- `tree2_model.pickle`  
- `rf2_model.pickle`  
