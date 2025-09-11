# bushfire-alert-prediction
Predictive system for bushfire severity in Perth, developed using scraped social media data and weather datasets. This repository contains the data collection, dataset preparation, and model development workflow.

---

## Project Overview
Bushfires remain one of the most severe natural hazards in Western Australia, particularly in the Perth metropolitan area where nearly 75% of the state’s population resides. This project develops a predictive early-warning framework that classifies bushfire alerts into **Advice**, **Watch and Act**, or **Emergency Warning**, aligned with the **Australian Warning System (AWS)**.  

The framework integrates two key data sources:  
- **Bushfire alerts** from the Department of Fire and Emergency Services (DFES), collected via Twitter/X scraping.  
- **Meteorological observations** from the Bureau of Meteorology (BoM), including temperature, rainfall, wind, and sunshine.  

Machine learning models such as **Random Forest, Support Vector Machine, and XGBoost** were benchmarked, with **stacking ensemble methods** (e.g., XGBoost + LightGBM with Logistic Regression meta-learner) providing the best generalisation. The models also address **class imbalance** and include **feature importance analysis** to ensure interpretability for decision-makers.  

The end goal is to support emergency authorities and communities with a system that is both **technically robust** and **operationally interpretable**, helping anticipate dangerous conditions and improve bushfire preparedness in Perth and potentially other regions.

---

## Project Stages

### 1. Data Scraping
Notebook: **`1. data scraping.ipynb`**  
- Uses **Twitter API authentication token**.  
- Collects raw fire-related data from social media.  

### 2. Dataset Preparation
Notebook: **`2. Dataset.ipynb`**  
- Cleans the raw data.  
- Merges with additional datasets (`Burnt Areas.csv`, `cleanbushfire-martojan.csv`, etc.).  
- Prepares the final dataset for model training.  

### 3. Model Development
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
