# alert-prediction
Predictive system for bushfire severity in Perth, developed using scraped social media data and weather datasets. This repository contains the data collection, dataset preparation, and model development workflow.

---

## Project Stages

### 1.  Model Development
Notebook: **`3. Model.ipynb`**  
- Implements a **Stacking Ensemble Model**.  
- Base models: **XGBoost** and **LightGBM**.  
- Meta learner: **Gradient Boosting Classifier**.  
- Evaluated with metrics: **Accuracy, Precision, Recall, and F1-Score**.  

⚡ **Quick Tip**: Because the dataset is already prepared, you can skip directly to **`3. Model.ipynb`**.  

---

## Technologies and Libraries

**Language:** Python  

**Key Libraries:**
- `pandas`, `numpy` → Data manipulation and analysis  
- `matplotlib`, `seaborn` → Data visualization  
- `scikit-learn` → Machine learning model building and evaluation  
- `xgboost`, `lightgbm` → Ensemble base models  
- `playwright` → Data scraping  
---

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/jovi23f/bushfire-alert-prediction.git
   cd bushfire-alert-prediction
2. **Dependencies**
   You do not need a separate requirements.txt. All required libraries are already installed directly in the notebooks using pip install commands.
   If running in Google Colab, just run the notebooks from the first cell.
   If running locally, make sure you have Python 3.10+ and execute all cells including installation commands.
3. **Run the notebooks in sequence**
   
   a. data scraping.ipynb → Add your Twitter API token to authenticate.
   
   b. Dataset.ipynb → Clean and prepare the dataset

   c. Model.ipynb → Train and evaluate the model.
