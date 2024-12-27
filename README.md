# DS_Prediction

## Project Description
This project explores the relationships between vegetable prices and multiple factors such as weather, supply and demand, and fuel prices. It utilizes data to construct three price prediction models: XGBoost, SVR, and CNN+Transformer. The goal is to improve the accuracy of price predictions, enabling applications in agricultural planning, supply chain management, and policy-making.

## Data Sources
1. Agricultural Product Wholesale Market Trading Data
  -  Obtained from the Agricultural Marketing Information System (AMIS) website, which provides agricultural transaction data, including daily trading volumes, average prices, and market distributions.
2. Historical Fuel Price Data
  - Retrieved from the CPC Corporation, Taiwan website, offering historical data on gasoline and diesel prices.
3. Agricultural Meteorological Observation Network
  - Sourced from the Agricultural Meteorological Observation Network, jointly provided by the Central Weather Bureau and the Ministry of Agriculture. Includes data on temperature, rainfall, relative humidity, wind speed, and solar radiation.

## Data Collection and Preprocessing
1. Weather Feature Data:
  - Combined weekly meteorological data collected via web scraping from northern, central, southern, and eastern regions to unify weather data across Taiwan.
  - Checked for missing values in regional weather data and filled them using data from the previous week.
2. Vegetable Data:
  - Checked for missing values in the data of three types of vegetables and merged them into a unified dataset. Verified and removed duplicate records.
3. Gasoline and Diesel Price Data:
  - Checked for missing values and removed data where the date did not start on a Monday.
  - Merged the weather, vegetable, and fuel data into a single dataset. Split the dataset into training (train.csv) and testing (test.csv) sets with an 80:20 ratio using random_seed: 42.

# Price prediction models(model.ipynb)
This project involves predictive modeling to forecast the prices and trading volumes of various crops using machine learning techniques like XGBoost, Support Vector Regression (SVR), and Convolutional Neural Networks (CNN). The models utilize weather data, fuel prices, and historical crop prices to make predictions.
## Requirements
- Python 3.11.9

Required libraries:
- pandas
- numpy
- scikit-learn
- xgboost
- tensorflow
- joblib
## How to Run


1. Train Models:
This project uses three prediction models to forecast vegetable prices. The models utilize the preprocessed train.csv data as the training set and test.csv as the test dataset.
- XGBoost:

  - Use GridSearchCV for hyperparameter tuning.
  - Train separate models for cabbage, cauliflower, and Chinese cabbage prices.

- SVR:

  Alternative regression model with hyperparameter tuning.

- CNN+Transformer:

  A deep learning method that integrates convolutional and transformer-based architectures for advanced predictive modeling.

2. Evaluate Models:

- Metrics:

  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
  - R-square Score

# Project Structure
```plaintext
DS_Prediction/
├── collect-data-code-ipynb/
│   ├── Crawler_Fuel.ipynb
├── vegetable-csv/
│   ├── Domestic_Cabbage.csv
│   ├── Domestic_Cauliflower.csv
│   ├── Domestic_Chinese_cabbage.csv
├── weather-csv/
│   ├── central_weekly_averages.csv
│   ├── east_weekly_averages.csv
│   ├── north_weekly_averages.csv
│   ├── south_weekly_averages.csv
├── Data_Analysis.ipynb
├── fuel_prices.csv
├── model.ipynb
├── test.csv
├── train.csv
├── ...
```
