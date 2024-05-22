# Climate
## Description
Data Science project to investigate sea surface temperatures in time series.

Spectral analysis on 80 years of sea surface temperatures in the North Pacific Ocean was done first using a discrete fourier transform. The most prevalent frequencies were determined, before a low-pass butterworth filter was applied to reduce the noise of frequencies from periods less than one year. The most prevalent frequencies in the filtered data were determined. Then, many autoregression models were trained on the data using various k/lags. The model with the lowest mse on the testing data was then tasked with predicting sea surface temperatures 20 years into the future. See `Climate_Data_Analysis.ipynb` for the full analysis.

## Report
'climate_report.docx' contains the full report on the results of the analysis.

## Analysis
`Climate_Data_Analysis.ipynb` is the notebook that contains the full analysis.

## Data Preparation
The notebook `Climate_Data_Analysis.ipynb` was used prepare data. The notable preparatins made were:
*  All columns other than sea surface temperatures (sst) were dropped.
*  A low-pass butterworth filter was applied using a frequency of one over one year.

## Data Source
### climate data
The climate data is over 80 years of daily sea surface temperature, wave height, and wind speed data from the North Pacific Ocean. The data has been queried from the [ERA5 Reanalysis Product](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=overview).

A reanalysis is a dataset that combines historical observations with a physics-based computer model of the earth system (which is not generally as accurate as a measurement, but can at least cover the entire world) to produce consistent yet large datasets. ERA5 is produced by the European Center for Medium-Range Weather Forecasting (ECMWF), widely regarded as the best forecasting center in the world. Therefore, it is the preferred data product for studying how the Earth's climate has evolved over the past century. 

The variable we will be interested in using is sst, which is the sea surface temperature in Kelvin.

Downloaded from: (https://github.com/galenegan/DATA-3320/blob/main/climate/north_pacific.csv)


## Author and License
Created by Lily Bleicher on 5/21/2024.
Feel free to use or modify with credit.
