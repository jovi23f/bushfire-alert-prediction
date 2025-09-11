# alert-prediction
Predictive system for fire alert levels in Perth, developed using historical alert messages and weather datasets.  
This repository contains the dataset and the machine learning model for classification.

---

## Model Development
Notebook: **`3. Model.ipynb`**  
- Evaluates **SVM**, **Random Forest**, and **XGBoost** classifiers.  
- Implements **Stacking Ensembles** with different base learners and meta learners:  
  - Base models: SVM + RF, or XGBoost + LightGBM  
  - Meta learners: Logistic Regression, Gradient Boosting, XGBoost, LightGBM  
- Models evaluated with metrics: **Accuracy, Precision, Recall, and F1-Score**.  

---

## Technologies and Libraries

**Language:** Python  

**Key Libraries:**
- `pandas`, `numpy` → Data manipulation and analysis  
- `matplotlib`, `seaborn` → Data visualization  
- `scikit-learn` → Machine learning model building and evaluation  
- `xgboost`, `lightgbm` → Ensemble base models  
---

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/jovi23f/alert-prediction.git
   cd alert-prediction
2. **Dependencies**
   You do not need a separate requirements.txt. All required libraries are already installed directly in the notebooks using pip install commands.
   If running in Google Colab, just run the notebooks from the first cell.
   If running locally, make sure you have Python 3.10+ and execute all cells including installation commands.
3. **Run the notebooks**
   Open and run 3. Model.ipynb to train and evaluate the model.

