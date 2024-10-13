# Detecting Moisture Transport Features using Machine Learning

Here, apply the CGNet / ClimateNet neural network ( https://github.com/andregraubner/ClimateNet; https://portal.nersc.gov/project/ClimateNet/; Higgins et al. 2022, https://doi.org/10.1029/2022MS003495) for detection of moisture transport anomaly features in ERA5. 

First, i run the MOAAP tool (Prein et al. 2023, https://doi.org/10.1029/2023EF003534; https://github.com/AndreasPrein/MOAAP) to obtain labeleled IVT objects (column-integrated water vapor transport) for April 2019. This is used as the reference data to train the neural network, together with column-integrated water vapor (tcvw) and horizontal wind speed components at 850 hPa from ERA5, on 6 hourly basis. 

The model is then used to predict IVT objects for April 2020, compared to results from MOAAP.

This approach could potentially be developed further to identify Arctic warm and moist air intrusions in regional climate simulation output from the PolarRES project with low computational effort in cases when true IVT output is not available from all RCMs.  
