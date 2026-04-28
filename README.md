# Milestone-2 Presentation
This repository contains the Milestone 2 Presentation for CSCI-7090: Data Science &amp; Machine Learning (Spring 2026)


This repository contains the Milestone 2 Presentation deliverables for CSCI-7090: Data Science & Machine Learning (Spring 2026).
The focus of this milestone is to present our data collection, wrangling, exploratory data analysis (EDA), and intermediate ML insights, preparing for predictive modeling in Milestone 3.


# Team 10 – CSCI-7090: Data Collection, Wrangling, and Visualization (Milestone 2)
Members: 
- Md Rajaul Karim
- Md Jahidul Islam

The primary goal of this milestone is to demonstrate the ability to:  
- Acquire and document a real-world dataset relevant to our research topic.  
- Clean, preprocess, and engineer features to produce an analysis-ready dataset.  
- Explore and visualize the data to uncover patterns, relationships, and insights.  

---

## Repository Structure

├── Codes<br>
├    ├──SOTA Comp AWQI.ipynb<br>
├    ├──SOTA Comp DWQI.ipynb<br>
├    ├──SOTA Comp IWQI.ipynb<br>
├    ├──SOTA Comp IndWQI.ipynb<br>
├    ├──EDA_for_ML_Model_DSML.ipynb<br>
├<br>
├── Datasets<br>
├    ├──Milestone II.csv<br>
├<br>
├── Exported PDF for Codes<br>
├    ├──SOTA Comp AWQI.ipynb.pdf<br>
├    ├──SOTA Comp DWQI.ipynb.pdf<br>
├    ├──SOTA Comp IWQI.ipynb.pdf<br>
├    ├──SOTA Comp IndWQI.ipynb.pdf<br>
├    ├──EDA_for_ML_Model_DSML.ipynb - Colab.pdf<br>
├<br>
├── Latex File\Water_Quality_Index_Prediction_Using Machine Learnig.zip<br>
├── Milestone- II.pptx<br>
├── Report File Latex Milestrone 2.pdf<br>
└── README.md


- To run all ML code, such as `SOTA Comp AWQI.ipynb` file, you need to use `Milestone II.csv` dataset.

---

# How to Run/Reproduce outputs using code(.ipynb) in Google Colab with the given Datasets and codes


## Open Notebook in Google Colab

1. Go to https://colab.research.google.com/
2. Click **File → Upload notebook**
3. Upload any of the notebook `.ipynb` file  

---

## 📂 Adding Respective Dataset with the Code


### Option 1: Upload Dataset


```python
from google.colab import files
uploaded = files.upload()
```

Then load it:

```python
import pandas as pd
df = pd.read_csv("Milestone II.csv")
```

### Option 2: Use Google Drive (Recommended)

```python
from google.colab import drive
drive.mount('/content/drive')
```

Authorize access, then load the dataset:

```python
import pandas as pd
df = pd.read_csv('/content/drive/MyDrive/path_to_your_dataset/Milestone II.csv')
```

▶️ Running the Notebook

- Run all cells: Runtime → Run all
- Run individual cells: Shift + Enter

---

# How to Run Latex Project Using Overleaf
You need to download the `Water_Quality_Index_Prediction_Using Machine Learnig.zip` file from the `Latex File` folder from this repository. Then follow these simple following steps:

- Go to https://www.overleaf.com/
- Click New Project → Upload Project
- Upload the .zip file
- The project will automatically compile

---
---

## Data Operations Competed in this Miltestone 

The dataset was cleaned and prepared for analysis through the following steps:  

1. **Missing Value Analysis:** Identified missing values and applied appropriate imputation strategies (mean/median/mode imputation, forward/backward fill, or deletion).  
2. **Data Type Conversion:** Ensured correct types, converted date strings to datetime, and encoded categorical variables (label encoding or one-hot encoding).  
3. **Outlier Detection and Treatment:** Detected outliers using IQR and Z-score methods; treated them by removal or capping with justification.  
4. **Feature Engineering:** Created new features such as [feature examples] to enhance model performance.  
5. **Normalization/Scaling:** Applied [StandardScaler / MinMaxScaler / RobustScaler] to numerical features for consistent range and distribution.  
6. **Final Dataset Summary:** Compared dataset shape, missing values, and descriptive statistics before and after wrangling.

---

## Exploratory Data Analysis (EDA) & Visualizations

Visualizations were created to uncover patterns, relationships, and trends:  

- **Distribution Plots:** Histograms/KDE plots for key numerical features.  
- **Correlation Heatmap:** Highlighting relationships between features.  
- **Categorical Analysis:** Bar charts, count plots, and pie charts for categorical variables.  
- **Feature Relationships:** Scatter plots or pair plots for interactions and target variable relationships.  
- **Time Series / Specialized Plots:** Trend visualizations, geographic plots, or alternative visualizations appropriate to the dataset.  

All visualizations are publication-quality with clear titles, labeled axes, consistent color schemes, and interpretation text accompanying each figure.

## Water Quality Index Model Implemented

- **AWQI:** Aquaculture Water Quality Index
- **DWQI:** Drinking Water Quality Index 
- **IWQI:** Irrigation Water Quality Index 
- **IndWQI:** Industrial Water Quality Index 

## Proposed Model Architecture

The proposed framework combines temporal modeling, attention mechanisms, and multi-task learning:

# Input:
- 10 physicochemical parameters
# LSTM Layers:
- First layer captures basic feature dependencies
- Second layer learns deeper nonlinear relationships
# Multi-Head Attention:
- Identifies important feature interactions
- Improves interpretability by weighting key parameters
# Pooling Layer:
- Converts sequence output into a shared representation
# Multi-Task Output Heads:
- Simultaneously predict IndWQI, IWQI, DWQI, and AWQI


## Existing Baseline (following) Comparison with Proposed Method:

- Ridge Regression
- Lasso Regression
- Linear Regression
- Decision Tree Regressor
- Random Fores Regressor
- XGB Regressor
- Gradiant Boosting Regressor
- LightBGM Regressor
- KNN Regressor
- MLP Regressor 


## Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score
