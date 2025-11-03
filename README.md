# Undervalued NBA Players 2009 to 2018
Goal: Use machine learning to estimate what an NBA player should have been paid based on performance, and identify players who were undervalued.

# Overview

This project combines two datasets from Kaggle (player performance + salaries), cleans and merges them, trains regression models, and outputs a list of players whose predicted salary is higher than what they were actually paid.

ValueScore = Predicted Salary − Actual Salary

Positive ValueScore → undervalued
Negative → overpaid



# What the project does

1. Load salary and player performance data from Kaggle
2. Clean and normalize the data
3. Merge both datasets using player_id
4. Train two models:
- Linear Regression
- Random Forest Regressor
5. Evaluate which predicts salary better
6. Calculate ValueScore for every player
7. Output the top undervalued players


# Key Takeaways

1. Random Forest performed better than Linear Regression

2. Career Win Shares (career_WS) was the most predictive feature

3. The year of the season (season_end) matters because salaries inflate over time as the NBA salary cap increases

# Top Undervalued Players (based on model prediction)
| Player       | Season  | Salary | Predicted | ValueScore |
| ------------ | ------- | ------ | --------- | ---------- |
| Vince Carter | 2011–12 | $3.0M  | $7.76M    | +$4.76M    |
| Brandon Roy  | 2012–13 | $5.1M  | $9.46M    | +$4.36M    |
| Greg Monroe  | 2017–18 | $5.0M  | $9.28M    | +$4.28M    |
More results are in CSV Output



# Feature importance (Random Forest):

Shows which statistics matter most for predicting salary.

1. career_WS 
2. season_end
3. career_PTS
4. career_PER
5. career_TRB
6. career_AST


# Future Work

Normalize salary by % of salary cap instead of raw dollars

Add features like position, draft pick, and experience

Try additional models like XGBoost

