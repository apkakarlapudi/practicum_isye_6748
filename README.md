# practicum_isye_6748
Sandia National Labs Practicum

## Data Files*
1. csv_files folder contains all CSV's with charge, discharge and impedance data
2. extra_data_info folder contains detailed information about specific CSV files, including details about the fields inside the CSVs
3. meta_data_files folder contains metadata files after feature engineering (code to run can be found inside battery_analysis_feature_engineering.ipynb)
* All data in the folder was uploaded after cleaning and transforming from original matlab version

## Jupyter Notebook Files
1. battery_analysis_charge.ipynb - Runs EDA and model selection for charge cycles
2. battery_analysis_discharge.ipynb - Runs EDA and model selection for discharge cycles
3. battery_analysis_EDA.ipynb - Runs EDA on general data
4. battery_analysis_feature_engineering.ipynb - Generates new metadata files to run analysis on
5. battery_analysis_impedance.ipynb - EDA and model implementation on impedance data

## Images
Folder contains all images generated from exploratory data analysis and model visualizations

Packages Required to Run Notebooks:
numpy, pandas, seaborn, os, tdqm, matplotlib, scikit-learn, xgboost
