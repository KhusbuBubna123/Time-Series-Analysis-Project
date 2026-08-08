<img width="222" height="148" alt="rainfall_image" src="https://github.com/user-attachments/assets/0b5852b0-e48d-4752-88b7-5a38151259f8" />

In this Project, Time Series Analysis was performed to on Mumbai City's monthly rainfall dataset(Source:Kaggle) using Arima,
AUTO Arima(Using Best Orders predicted by Auto Arima),Sarima (Seasonal Arima), Auto Sarima, LSTM. Also XGBoost 
& LightGBM Machine Leaning Models were also used. 

The dataset contains detailed monthly rainfall records for Mumbai, a city known for its intense monsoon season. 
It offers insights into the rainfall patterns over time, helping researchers, data enthusiasts, and climate analysts
explore trends, seasonal variations, and extreme weather events. The data is sourced from OpenCity and is in the 
Public Domain. 

Key Features: \
Location: Mumbai, India \
Time Period: 1901 to 2021- \
Data: Monthly rainfall (in mm) \
Attributes: Year, Month, Total Rainfall

The dataset was Seasonal.(Had Seasonality) so ARIMA did not perform so well. SARIMA performed better. Also Rainfall 
forecasting was done for years(24-Month (2 years) Forecast (1904–1906)) using SARIMA Model. For convenience, in this 
project time series analysis was performed on only a subset of dataset i.e.three years January-1901--December-1903. \


**Results:**
The results for Rainfall prediction(in mm) obtained(for years(24-Month (2 years) Forecast (1904–1906)) using SARIMA Model were as follows:


Forecast Table (1904–1906): \
 Month           Forecast     Lower 95%     Upper 95% 

Jan 1904              1            0          17  \
Feb 1904              1            0          21 \ 
Mar 1904              1            0           46 \
Apr 1904              1            0           74 \
May 1904              1            0           248 \
Jun 1904             169           1        51436  \
Jul 1904             311           1        141596 \
Aug 1904             354           1       233806 \
Sep 1904             327           0        308457 \
Oct 1904             28            0         36878 \
Nov 1904         |      0     |        0    |       665 \
Dec 1904          |     5     |        0     |    13359 \
Jan 1905         |      1     |        0     |     2459
Feb 1905          |     1      |       0     |     3480
Mar 1905         |      0      |       0     |     4852
Apr 1905        |       1      |       0      |    8167
May 1905        |      33      |       0       754818
Jun 1905        |     184      |       0      6029424
Jul 1905        |     416      |       0     19532049
Aug 1905        |     321       |      0     21339585
Sep 1905       |      172      |       0     16080577
Oct 1905       |       61     |        0      7886173
Nov 1905        |       0     |        0        83629
Dec 1905        |       1     |        0       236266

<img width="1515" height="745" alt="graph-Sarima" src="https://github.com/user-attachments/assets/ff4a63de-acce-42b2-8094-002a0d492b41" />

We have also compared differenet model in terms of Mean Absoulute Error and Root Mean Square Error \

                          Rank      MAE     RMSE  MAPE
Holt-Winters Additive        1    86.70   123.45   inf. \
XGBoost                      2   206.21   313.71   NaN. \
Holt Linear                  3   209.55   336.06   inf \
Simple Exp Smoothing         4   209.83   337.22   inf. \
LSTM                         5   209.93   341.94   inf  \
ARIMA(2,1,1)                 6   211.37   329.26   inf \
auto_ARIMA(2, 0, 0)          7   218.59   340.71   inf. \
