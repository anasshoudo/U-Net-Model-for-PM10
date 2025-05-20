# U-Net-Model-for-PM10
This notebook contains the implementation of U-Net used in (Houdou et al., 2025) to forecast PM10 values in Morocco.

The notebook uses pre-prepared data from Copernicus Atmosphere Monitoring Service (CAMS). The data is of two kinds: one is the reanalysis data, which serves as observational or reference data and contains concentrations of PM10. The other is forecast data, provided in the form of 8 NetCDF files containing forecasts for 8 predictors:

- PM10 – Particulate Matter with aerodynamic diameter ≤10 µm
- PM2.5 – Particulate Matter with aerodynamic diameter ≤2.5 µm
- PM1 – Particulate Matter with aerodynamic diameter ≤1 µm
- DAOD – Dust Aerosol Optical Depth at 550 nm
- 2mT – Temperature at 2 meters above the surface
- U10 – Zonal (east-west) wind component at 10 meters
- V10 – Meridional (north-south) wind component at 10 meters
- BLH – Boundary Layer Height

The data spans from 2015 to 2023, covering the entire domain of Morocco.

The forecast files are structured as follows:

- 3,287 forecast reference times (initialization days)
- 5 forecast periods (daily lead times)
- 43 latitude points
- 46 longitude points
  
The reanalysis data is structured as follows:

- 3,287 forecast reference times (initialization days)
- 5 forecast periods (daily lead times)
- 22 latitude points
- 23 longitude points

The reanalysis data was restructured to match the forecast data. Details about the processing steps can be found in (Houdou et al., 2025).

The TensorFlow framework version 2.17.0 was used to train the U-Net models.



### References

Houdou, A., Khomsi, K., Delle Monache, L., Hu, W., Boutayeb, S., Belyamani, L., Abdulla, F., El Badisy, I., Al-Delaimy, W. K., & Khalis, M. (2025). Enhancing 5-Day Particulate Matter (Pm10) Forecasts in Morocco Using U-Net: A Deep Learning Approach. SSRN. https://doi.org/10.2139/ssrn.5191935
