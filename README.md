# My-thesis

This project contains two separate python script files and one GJSON point file for the diploma thesis titled  “Research on the relationship of Methane concentrations with other atmospheric pollutants and parameters through multidimensional analysis of Sentinel-5P data”. For more details you can read the full thesis at the following URL:

## Python script: "Download_atmospheric_data"

- Based on the requirements of the thesis, this project focuses on the following atmospheric gases and parameters of Sentinel-5p: CH4, CO, NO2, SO2, HCHO, aerosol index, cloud fraction (aerosol height was exported but not used in the atmospheric analysis).
- All the atmospheric data were downloaded using Google Earth Engine, hence authentication is required by running ee.Authenticate() function. A Google Earth Engine prject is also needed.
- The aforementioned atmospheric data were exported for specific points of interest, contained in the Gas_plants_units_2024_fin GeoJON file. Those points (14 in total) mainly refer to Gas plants, with a few oil and coal plants in the Greek area, sourced from Global Energy Monitor for the year 2024. Sentinel-5p data were exported for 2023 in the form of Excel files for each plant station.
- CH4 data were combined from each station due to lack of original CH4 Sentinel-5p data
