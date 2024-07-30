# **Predicting Olympic medals**
# Hypothesis
Predicting the number of medals a country will win at the Olympics using historical data.
# Data
## Dataset: Historical data of Olympic medals won by countries.
### Key Features :
- Number of athletes (athletes)
- Average age of athletes (age)
- Previous medals won (prev_medals)
## Data Preprocessing
### 1. Loaded Data: 
Data was loaded into a pandas DataFrame.
### 2. Handled Missing Values: 
Dropped rows with missing values.
### 3. Data Split:
◦ Training set: Data before 2012.
◦ Testing set: Data from 2012 onwards.
## Exploratory Data Analysis (EDA)
### Correlation Analysis: 
Athletes (0.84) and prev_medals (0.92) have strong positive correlations with medals
### Visualizations:
◦ Scatter plots for athletes vs.
medals and age vs. medals
◦ Histogram of medals distribution.
## Model Training
### Model: 
Linear Regression
### Predictors: 
athletes, prev_medals
### Training:
    from sklearn.linear_model import LinearRegression'
    reg = LinearRegression()
    reg.fit(train[predictors]
    train["medals"]) '''
# Predictions and Evaluation
## Predictions:
    predictions = reg.predict(test[predictors])
    test["predictions"] = predictions.clip(min=0).round()
### Mean Absolute Error: 3.30
# Results
The model performs well for countries with high medal counts.
### USA Prediction: 
2016 prediction was close to actual (264 vs. 235.57)
### India Prediction: 
Overestimated in 2016 (2 actual vs. 11.68 predicted).
# Next Steps
### Additional Features: 
Include height, number of years competing.
### Athlete-Level Analysis: 
Utilize detailed athlete data.
### Improved Modelling: 
Focus on low medal count countries with event-specific models.
# Conclusion
The model effectively predicts medal counts for high-performing countries. Further refinem must needed for countries with low medals. 
