# Ames-Iowa-Housing-ML-Project
Group project 

Goal of project is to 
  - predict housing saleprice for home buyers and sellers
  - determine home attributes impacting price
  - gather insights into the market in Ames, Iowa

Background

Data set covers property sale between 2006 and 2010. Exclusing PID and SalePrice, the dataset contains 79 original features.
Demographically, Ames comprosise of students, professors and their families. The largest employer is Iowa State Univerity.

Data Cleaning

Housing and real estate files were merged on PID and GeoRefNo to obtain lon and lat

NaN handled
  - Categorical filled with "missing"
  - Numeric filled with mean/mode/median

Feature engineering
  - features created include "TotalSF", "DistanceToISU", "DistanceCategory", "Season"

Linear models used including multiple linear and lasso regression

Lasso
1. All features needed to be in int or float type before modeling. Nominal features were dummified with first column KEPT. Lasso can handle multicollinearity. Ordinal features were mapped based on ranking (missing=0)
2. Standard Scaler applied ensures features are equally contributing to computation
3. K-fold cross-validation used to improve model performance
4. GridSearch used to determine best alpha, a regularization term to reduce/shrink features to 0 if they do not contribute much to the model

Multiple Linear Regression
1. Standard scaler was not applied so the coefficients could be more interpretable
2. Dummified categorical features - first columns were dropped. The first column increases multicollinearity
3. Lasso was used to select important features, then fed into the lienar model

Quick notes
Removing outliers can increase r2; however, the outliers are interesting data points themselves. They signify which houses were under/oversold and could be potential opportunies for buying and selling homes.
    
   
