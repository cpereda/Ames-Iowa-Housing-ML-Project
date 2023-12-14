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
