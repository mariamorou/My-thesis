# My-thesis

This project contains two separate python script files and one GeoJSON point file for the diploma thesis titled  **“Research on the relationship of Methane concentrations with other atmospheric pollutants and parameters through multidimensional analysis of Sentinel-5P data”**. Based on the requirements of the thesis, this project focuses on the following atmospheric gases and parameters of Sentinel-5p: CH4, CO, NO2, SO2, HCHO, aerosol index, cloud fraction (aerosol height was exported but not used in the atmospheric analysis). Current thesis focuses on the research of the relationship of CH4 with the rest of the atmospheric variables. For more details you can read the full thesis at the following URL:

## Python script: "Download_atmospheric_data"
- This script focuses on the exportation of atmospheric parameters of interest. All the atmospheric data were downloaded using Google Earth Engine, hence authentication is required by running ee.Authenticate() function. A Google Earth Engine project is also needed.
  
- The aforementioned atmospheric data were exported for specific points of interest, contained in the Gas_plants_units_2024_fin GeoJON file. Those points (14 in total) mainly refer to Gas plants, with a few oil and coal plants in the Greek area, sourced from Global Energy Monitor for the year 2024. Sentinel-5p data were exported for 2023 in the form of Excel files for each plant station.
  
- CH4 data were combined from each station due to lack of original CH4 Sentinel-5p data

## Python script: "Data_analysis"
- Data_analysis script is a continuation of the previous script. It includes data imputation and preparation for the statistical analysis that was conducted. Specifically, apart from statistical models, the following statistical tests and data analyses were applied:
  
  1. **Kalman imputation:** Kalman filter was implemented in order to calculate missing data values of 2023 for each atmospheric daily timeseries.
  2. **ADF test:** Augmented Dickey–Fuller test was applied in order to test stationarity for each timeseries
  3. **VIF test:** Variance inflation factor was used to check for multicollinearity, among the independent variables
  4. **AIC criterion:** AIC criterion was applied in order to compute best lag value for Granger causality test

- A series of linear and non-linear models were applied, assuming that CH4 is the dependenet variable and the rest of the Sentinel-5p parameters as independent variables: linear model, generalized linear model, linear model with interaction terms, polynomial model and random forest model. Apart from the statistical results, the following graphs were created: Residuals vs Fitted values, Q-Q plot, Scale-Location and Interaction plot (for the model with interaction terms)
 
- In addition to the models, Granger causality test was performed

 

