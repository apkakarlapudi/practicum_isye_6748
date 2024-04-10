# practicum_isye_6748
Sandia National Labs Practicum

## Data Files*
1. csv_files folder contains all CSV's with charge, discharge and impedance data
2. extra_data_info folder contains detailed information about specific CSV files, including details about the fields inside the CSVs
3. meta_data_files folder contains metadata files after feature engineering (code to run can be found inside battery_analysis_feature_engineering.ipynb)
* All data in the folder was uploaded after cleaning and transforming from original matlab version

Field information:
Data Structure:
- cycle:	top level structure array containing the charge, discharge and impedance operations
	- type: 	operation  type, can be charge, discharge or impedance
	- ambient_temperature:	ambient temperature (degree C)
	- time: 	the date and time of the start of the cycle, in MATLAB  date vector format
	- data:	data structure containing the measurements
	   - for charge the fields are:
		- Voltage_measured: 	Battery terminal voltage (Volts)
		- Current_measured:	Battery output current (Amps)
		- Temperature_measured: 	Battery temperature (degree C)
		- Current_charge:		Current measured at charger (Amps)
		- Voltage_charge:		Voltage measured at charger (Volts)
		- Time:			Time vector for the cycle (secs)
	   - for discharge the fields are:
		- Voltage_measured: 	Battery terminal voltage (Volts)
		- Current_measured:	Battery output current (Amps)
		- Temperature_measured: 	Battery temperature (degree C)
		- Current_charge:		Current measured at load (Amps)
		- Voltage_charge:		Voltage measured at load (Volts)
		- Time:			Time vector for the cycle (secs)
		- Capacity:		Battery capacity (Ahr) for discharge till 2.7V 
	   - for impedance the fields are:
		- Sense_current:		Current in sense branch (Amps)
		- Battery_current:	Current in battery branch (Amps)
		- Current_ratio:		Ratio of the above currents 
		- Battery_impedance:	Battery impedance (Ohms) computed from raw data
		- Rectified_impedance:	Calibrated and smoothed battery impedance (Ohms) 
		- Re:			Estimated electrolyte resistance (Ohms)
		- Rct:			Estimated charge transfer resistance (Ohms)

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
