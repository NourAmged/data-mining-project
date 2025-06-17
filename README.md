# Crime Rate Data Mining Project

## Overview
This project analyzes and models crime data using data mining techniques. The workflow includes data preprocessing, clustering, classification, and visualization to extract insights from crime records. The main work is implemented in the Jupyter notebook `Crime-Rate-Project.ipynb`.

## Dataset
- **Source:** `train.csv` (compressed as `train.csv.zip`)
- **Description:** Contains crime records with features such as date, location (X, Y), category, police district, and address.

## Main Steps

### 1. Data Preprocessing
- Loaded and cleaned the dataset (handled missing values and duplicates).
- Encoded categorical variables (e.g., `Category`, `PdDistrict`, `Address`).
- Extracted date features (year, month, day) and dropped unnecessary columns.
- Applied standard scaling (z-score normalization) to location features.

### 2. Clustering (K-Medoids)
- Filtered data for the year 2015 to reduce size.
- Applied K-Medoids clustering on scaled location features (`X_scaled`, `Y_scaled`).
- Used the elbow method to determine the optimal number of clusters.
- Evaluated clustering using the Silhouette Score.
- Visualized clusters on a map.

### 3. Classification (Random Forest)
- Used Random Forest Classifier with entropy as the criterion.
- Dropped location columns for classification.
- Evaluated model using log loss on training and test sets.

### 4. Data Visualization
- Plotted crime counts per month and year.
- Visualized the distribution of crimes by police district and top 10 crime categories using pie charts.

## Requirements
- Python 3.x
- Jupyter Notebook
- pandas, numpy, matplotlib, seaborn, scikit-learn, scikit-learn-extra, plotly

## How to Run
1. Unzip `train.csv.zip` to get `train.csv` in the project directory.
2. Open `Crime-Rate-Project.ipynb` in Jupyter Notebook.
3. Run the notebook cells sequentially to reproduce the analysis and visualizations.

## Results & Insights
- Identified optimal clusters of crime locations for 2015.
- Built a classification model to predict crime categories.
- Provided visual insights into crime patterns by time, location, and type.

