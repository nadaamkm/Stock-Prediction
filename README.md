# Stock-Prediction

The objective of this model is to predict the Microsoft stocks. 

I use time series decomposition to break up a time series into trend, seasonality, and residuals.

Time series decomposition is used in time series analysis for tasks such as:

- exploratory data analysis (e.g., has unemployment increased this quarter after adjusting for seasonality?);

- pre-processing time series to identify and impute outliers and missing data;

- extracting features from time series for later use in classification, regression, and forecasting tasks;

- building forecasts (e.g., the components can be forecasted separately and then aggregated to produce the final forecast).

I compare this to another simple model for prediction
Steps:

Set up a pipeline using the Pipeline object from sklearn.pipeline
Pipelines are used to automate a machine learning workflow. The pipeline can involve pre-processing, feature selection, classification/ regression and post-processing.

Perform a grid search for the best parameters using GridSearchCV()
Optimization tunes the model for the best performance. The success of any learning model rests on the selection of the best parameters that give the best possible results.

Analyze the results and visualize
Scaler: For pre-processing data, i.e., transform the data to zero mean and unit variance using the StandardScaler().

We also built two classifiers: Random Forest and KNN.


## Results

Summary of the ARIMA code We split the training dataset into train and test sets and we use the train set to fit the model, and generate a prediction for each element on the test set.

A rolling forecasting procedure is required given the dependence on observations in prior time steps for differencing and the AR model. To this end, we re-create the ARIMA model after each new observation is received.

Finally, we manually keep track of all observations in a list called history that is seeded with the training data and to which new observations are appended at each iteration.

Testing Mean Squared Error is 741.0594879572484

Summary for the second model using standard scalar and ridge regression is as follows:
Training set score: 0.9999075445887593
Test set score: 0.9999116106944692
Test MSE: 0.21098532111095497
Best Alpha: 0.001
Training set score: 0.9999509222922162
Test set score: 0.9999501290091789
R2: 100.0%

The results for KNN classification was disappointing; however, the Random Forest Classifier gave us an accuracy of 0.8247.


