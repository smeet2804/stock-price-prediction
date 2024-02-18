# Comparision of various ML Models for Stock Price Prediction 

## Introduction:
We compared various Machine Learning models like LSTM, SVM, CNN, and Linear Regression for predicting stock prices. Our primary focus area was to implement the models and try to predict the future Stock Price on the basis of previous year data. 

After implementing the models, we compared the models on the basis of various statistical parameters like RMSE (Root Mean Square Error), MSE (Mean Square Error) and MAE (Mean Absolute Error). 

After successfully completing the above, we tried to inculcate the sentimental parameters and implement the model along with the sentimental parameters and find the results. Finally, we would compare the results with and without the sentiments for various ML models mentioned above.

## Sentimental Analysis on the News Headlines:
We scraped all the news related to given company (INFOSYS) for a given time period and after preprocessing the data we selected the required columns. Concatenating all news headlines if they are more than one for a particular date, we performed the sentimental analysis on headlines. Last thing we did was finding the polarity score on headlines.

## The Scraped News Headlines:

![Picture1](https://user-images.githubusercontent.com/62166762/212843077-bcf72790-3e24-4133-a379-7f92bed6171c.png)

## Final Dataset: 

![Picture2](https://user-images.githubusercontent.com/62166762/212843361-89480be2-a178-4157-86ee-e8030f826e00.png)

## Comparision of Models (Without Sentiments):

![image](https://user-images.githubusercontent.com/62166762/212843635-7d2c60c9-1002-4036-a54a-3802d55a6656.png)

## Result Metrics Comparison (without Sentiments)

|   | RMSE | MSE | MAPE
|---|---|---|---|
|LSTM|27.3201|746.38|23.15|
|CNN|30.9335|956.88|25.11|
|Linear Regression|97.08|9426.39|6.8|
|SVM|41.53|1725.075|2.4|

## Comparision of Models (With Sentiments):

![image](https://user-images.githubusercontent.com/62166762/212846738-bd813f23-0b2f-4304-8269-3698c92f0b51.png)

## Result Metrics Comparison (without Sentiments)

|   | RMSE | MSE | MAPE
|---|---|---|---|
|LSTM|42.85|1836.43|27.24|
|CNN|80.88|6941.75|71.10|
|Linear Regression|96.79|9369.46|6.8|
|SVM|43.51|1893.12|2.4|

## Pearson Correlation:

The strength of the association between two variables.

![image](https://user-images.githubusercontent.com/62166762/212847932-28ab0f0b-a375-4307-95ed-ccf364398be0.png)

r takes value between -1 (negative correlation) and 1 (positive correlation).
r = 0 means no correlation.

Pearson Correlation Metrics (INFOSYS):

||Positive|Negative|Neutral|Compound|
|---|---|---|---|---|
|Close Price|0.220|-0.282|-0.059|0.304|

## Conclusion:

LSTM gives better results in comparison to other models.

Linear Regression and SVM models can work better on companies which has linear growth over a period of time. Linear Regression model can be helpful in predicting  the trend of stock for a limited period of time.

There is weak correlation found between stock price and news headlines as per our findings.

The RMSE for models with larger duration (i.e. around a decade) are quite lower with that for a shorter duration in our case.

But, due to difficulty of gathering the sentiments for the stock we tried it for only one year.

Effect of sentiments on Stock Price is not clear and is still an area of research, and through our findings we can say that sentiments gathered from News Headlines have very little effect on the Stock Price Prediction.

All the models were implemented on HDFC Bank stock also and similar results were observed.
