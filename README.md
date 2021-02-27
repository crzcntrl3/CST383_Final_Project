# CST383_Final_Project

# NBA Win Prediction

Source:

February 10, 2021 from basketball-reference.com

[2018-2019 Season](https://www.basketball-reference.com/leagues/NBA_2019.html)

Video: 

[CST 383- Final Project Video](link)


## Introduction
For our final project, the objective was to predict the number of wins and NBA team would gain based on various features. The project was something that intrigued us both and we invisioned various avenues to take. With the given amount of time, we decided to predict NBA team wins based on a teams offensive and defensive rating. We also wanted to determine whether a previous team win had a direct correlation to the teams next win. This was all done with the purpose of gaining the skills to predict wins and losses based on simple features, and then later applying to more complicated predictions like whether an individual player can affect the outcome of a game.


## Selection of Data

This project originally consisted of 8 source of data/metadata, but we decided to cut it down to two sources in order to make the project more obtainable. We primarily focused on the main file **2018_2019_Misc.csv** that possesed 868 samples and 28 features.

We first removed some irrelevant features in regards to NBA win prediction: 'Rk','Age','MOV','SOS','SRS','NRtg','FTr','3PAr','TS%','eFG%','TOV%','ORB%','FT/FGA','eFG%.1','TOV%.1','DRB%','FT/FGA.1','Arena','Attend.','Attend./G'
because they were not going to be used to test what does/does not have an affect on team wins/losses. We also dropped the league average for now to ease the process.

The data has **five numeric features**:'ORtg','DRtg','W','L',and 'Pace' and **one categorical features**: 'Team'.

The other dataset, **2018_2019_WinsLosses.csv** was used to determine the outcome a previous win would have on the next, which possesed 6,560 samples and 5 features. The dataset was edited in excel, so we did not need to 'clean it up' as much. The data has **2 numeric features**: 'H_PTS' and 'V_PTS' and **3 categorical features**: 'Date', 'Visitor', and 'Home'.

We used **train_test_split** to prepare out datasets and build our models, but there seemed to be some issues as the outcome of the predictor was not was expected. Not to say it is impossible, but we kept obtaining an accuracy of **100%** which we could not figure out the cause.

## Methods:

**Tools:**

- Numpy, Pandas, Matplotlib, and Seaborn for data analysis and visualization
- Scikit-learn for inference
- Github for web app deployment and version control
- Anaconda for Juypter Notebook
- Colaboratory for collaboration efforts

**Inference methods used with Scikit:**

- Models: KNeighborsClassifier, KNeighborsRegressor, Anomolies, Linear Regression
- Features: train_test_split

## Results:
- Data exploration and Visualization
This produced rather visually applying results that displayed our desired outcome. Through the various plots we were able to visually represent the affect offensive and defensive rating had on team wins. The higher offensive rating typically resulted in a greater overall number of wins, the same could be determined when factoring in defensive rating. We were also able to conclude that the home team points scored did not always result in a win and that typically a winning home team averaged 118 points, while a visiting winning team averaged 110 points.
- Machine Learning/Predictions
This is where we could not really come to a conclusion, because after working with various models the accuracy still was calculated to be 100%. This could be due to various reasons, but due to time restraints we were not able to determine the cause. The predictor, predicted the same as the test set but the results were just not something we were expecting.

## Discussion:

This was a semi-succesful look into whether certain dataset features could have an affect on the outcome of a game between two teams.

During the data exploration and visulization, we were able to determine represent the relationships we were looking to test. In regards to the Misc. Stats dataset, we were able to see how good offensive and defensive rating would result in a better win/loss record. With more time permitted, an intriguing feature that would have been interesting to explore if it affected wins/losses was whether the amount possessions a team had resulted in more wins. Next was the wins & losses dataset, where we wanted to correlate whether the Home team won if they scored more points. The relation should this to be true but there were still a few interesting outliers, where the home team scored a lot but still ended up losing. The feature we would want to test next, is whether a previous win would result in better chances to win the next game. Overall the data exploration and visualization yield promising results.

The machine learning/prediciton is where the datasets came into question. There was 100% accuracy for both dataset when it came to predicting. Not to think that this is not possible, but it did not predict any team wins in the end results. This could be attributed to a wide varity of things such as dataset size, predictor values, also the training and test sets could be a reason. This was the most confusing part, as there were anomolies that were able to be accounted for but we could not determine the reason for such a high accuracy when predicting.

Overall the report yielded desired results, but maybe with more precise predictors/variables we would produce better predictions. For future work on these datasets, we would hope to provide better predictions and hopefully implement individual player efficiency datasets and determine whether a single player can have a overwhelming influence on the outcome of a game.

## Summary
To improve, we would hope to obtain more data over 5-10 season to provide an better/more accurate prediction. The most interesting thing we have taken away, is that in predicting team wins we whould rely on more than one season of data. We believe more features would also provide a more realistic outcome when predicting a teams wins/losses. The most interesting take-away was that a team was able to score 160 points and ended up losing anyways, this was visualized as an outlier in a boxplot. This was a fun project to try and implement, and overall we feel like we were able to prove the relations between various features and their affect on the teams win/loss outcomes. 
