# DS_Prediction
1. Report (in the format of pdf, better follow the standard paper format)

https://ncu365-my.sharepoint.com/:w:/r/personal/113522097_office365_ncu_edu_tw/Documents/Group6_Project_Report.docx?d=wf4baedfdb200498aaac71879b8643bf0&csf=1&web=1&e=qTrlxC

3. Video link of your presentation (please control in about 5 minutes, and upload to Youtube)
4. Presentation slide (in the format of ppt)

https://ncu365-my.sharepoint.com/:p:/r/personal/113522097_office365_ncu_edu_tw/Documents/Group6_Project_Slide.pptx?d=w8106d49f03cf4f74aae85a5db572bf78&csf=1&web=1&e=fmK1vj

6. Code & Instruction (How to reproduce your result)
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
# model.ipynb
This project involves predictive modeling to forecast the prices and trading volumes of various crops using machine learning techniques like XGBoost, Support Vector Regression (SVR), and Convolutional Neural Networks (CNN). The models utilize weather data, fuel prices, and historical crop prices to make predictions.
## Requirements
Python 3.7+
Required libraries:
pandas
numpy
scikit-learn
xgboost
tensorflow
joblib
## How to Run
Preprocess Data:
The script merges and processes weather, fuel, and crop data into a single dataset.
Missing values are handled via imputation and forward-fill techniques.
Extracted features include year, month, and week.
Train Models:
XGBoost:
Use GridSearchCV for hyperparameter tuning.
Train separate models for cabbage, cauliflower, and Chinese cabbage prices.
SVR:
Alternative regression model with hyperparameter tuning.
CNN+Transformer:
Deep learning approach for time-series prediction.
Evaluate Models:
Metrics:
Root Mean Squared Error (RMSE)
Mean Absolute Error (MAE)
R² Score
