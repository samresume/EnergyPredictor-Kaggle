# 🏢 ASHRAE - Great Energy Predictor III

## 🔍 Overview

This project addresses the challenge of predicting baseline energy usage in buildings for performance-based financing. Participants estimate what energy a building *would have used* without retrofits, enabling fair billing and encouraging investment in energy efficiency.

📎 [Kaggle Competition](https://www.kaggle.com/competitions/ashrae-energy-prediction)  
📎 [Dataset Download](https://www.kaggle.com/competitions/ashrae-energy-prediction/data)

---

## 📘 Notebook Objective

This notebook:
- Loads and explores the competition datasets
- Applies preprocessing and feature engineering
- Trains multiple machine learning models
- Evaluates models using RMSLE
- Generates predictions for Kaggle submission

> ✅ **Just run the notebook from top to bottom – no manual edits needed.**

---

## 📂 Files Used

- `train.csv`: Main training data with energy readings  
- `test.csv`: Test set for final prediction  
- `building_metadata.csv`: Metadata about buildings  
- `weather_train.csv` / `weather_test.csv`: Weather info over time  
- `sample_submission.csv`: Submission format template

---

## 🛠️ Libraries Used

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import zscore

from sklearn.model_selection import train_test_split
import xgboost as xgb
import lightgbm as lgb
```

---

## ⚙️ How to Run

1. Download all dataset files from the [Kaggle data page](https://www.kaggle.com/competitions/ashrae-energy-prediction/data).
2. Set your data path inside the notebook:

```python
path_data = "your/path/to/data/"
```

3. Run each cell in order from top to bottom.
4. A `submission.csv` file will be generated automatically.

---

## 📊 Evaluation

The official competition metric is:

**RMSLE** – Root Mean Squared Logarithmic Error

Used to fairly assess prediction accuracy while penalizing underestimates more than overestimates.

---

## ✅ Final Output

The notebook produces:
- Cleaned and preprocessed data
- Trained models with evaluation scores
- Kaggle-ready submission file
