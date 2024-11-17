# Weather_Forecasting
This project aims to forecast daily climate data using ARIMA models. The dataset used for this project is from Kaggle, which includes daily climate time series data. The main focus of this report is on forecasting the Humidity and Mean Temperature of the dataset. The methodology includes exploratory data analysis (EDA), data preprocessing, and the application of ARIMA models for both validation and forecasting.

## Dataset
Name: Daily_Climate.csv
Source: Kaggle - Daily Climate Time Series Data

The dataset consists of 1462 rows and 5 columns, with the following features:

- date: Date of the observation
- meantemp: Mean temperature (°C)
- humidity: Humidity (%)
- windspeed: Wind speed (km/h)
- meanpressure: Mean atmospheric pressure (hPa)

## Steps
### I. Exploratory Data Analysis (EDA)
The first step was to load the dataset and explore its basic properties. Key observations from the EDA include:

- No duplicate values were found in the dataset.
- The columns were of appropriate data types, with date being the only non-numeric feature.
- No missing values were present in the dataset.
- Descriptive statistics indicated no abnormal values, but scaling was applied to improve feature comparisons.

### II. Data Preprocessing
- Scaling: All numerical features were standardized using the StandardScaler. This was done to ensure that the features are comparable, especially since we are working with different units (e.g., temperature in °C and pressure in hPa).
- Outlier Removal: Several outliers in the humidity column were removed based on their extreme values.

### III. Feature Selection
For modeling, we focused on two features:

- Humidity: This feature was selected to explore its impact on climate forecasting.
- Mean Temperature: We also examined mean temperature, as it is closely related to climate behavior and forecasting.

### IV. ARIMA Model
The ARIMA (AutoRegressive Integrated Moving Average) model was used to forecast both Humidity and Mean Temperature. The process involved several steps:

- Stationarity Check: We used the Augmented Dickey-Fuller (ADF) test and the KPSS test to ensure the data was stationary. Both tests indicated that the data was stationary, allowing us to apply ARIMA modeling.
- Model Fitting: The ARIMA model was fit on the data using different configurations of parameters (p, d, q), based on the autocorrelation (ACF) and partial autocorrelation (PACF) plots.
- Model Validation: The model was validated using out-of-sample predictions and compared against the actual observed values.

### V. ARIMA Model Validation
The ARIMA model was evaluated by comparing the predicted values against actual values from the dataset. The following steps were taken:

- One-Step-Ahead Forecast: The model was used to forecast one step ahead, and the results were plotted alongside the actual data.
- Mean Squared Error (MSE): The model's forecasting accuracy was quantified using the Mean Squared Error (MSE), which provides a measure of the model's prediction accuracy.

### VI. ARIMA Forecasting
Once the model was validated, it was used to forecast future values of Humidity and Mean Temperature:

- Humidity Forecasting: Forecasts for the next 12 weeks were made and visualized.
- Mean Temperature Forecasting: A similar approach was applied to the mean temperature, forecasting the next 10 weeks.

### VII. Results
- Mean Squared Error (MSE): The MSE values for the models were calculated to assess the accuracy of the forecasts.
- Forecasting Performance: The ARIMA models for both features showed reasonable forecasting accuracy, with confidence intervals for the future predictions.

### VIII. Conclusion
- ARIMA Model Performance: The ARIMA models for both Humidity and Mean Temperature provided reasonable forecasts. The validation phase showed that the models could effectively predict short-term climate patterns.
- Further Improvement: The model performance could be improved by experimenting with different seasonalities, adding external regressors, or exploring more advanced models such as SARIMA (Seasonal ARIMA).
- Practical Applications: The forecasting of climate data can be useful for various industries such as agriculture, energy management, and environmental monitoring.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Requirements
To run this project, you need the following Python packages:

pandas
numpy
statsmodels
matplotlib
seaborn
scikit-learn

## Acknowledgements
The dataset is provided by Sumanth V Rao.

## Contact
For any inquiries or further information, please contact me at [tiz.berlanda@gmail.com].
