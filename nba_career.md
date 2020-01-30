## NBA Career Predictor

![](nba_career_gif.gif)

#### Summary:
How long will a player last in the NBA? This is a question asked by casual fans as well as scouts when evaluating NBA players from their early days on the court up to their tenth year in the league. With the NBA Career Predictor app, you can find out how long your favorite NBA players will last in the league. [VISIT APP HERE](https://nbacareerlength.netlify.com/), [VIEW CODE HERE](https://github.com/dcarter-ds/dcarter-ds.github.io/blob/master/NBA_Career_Longevity_Prediction_Carter.ipynb)

#### Technical Overview:
The goal of this project was to use Machine Learning models to predict NBA player longevity. The player data was mostly pulled and merged from two sources ([here](https://data.world/rvino88/1976-to-2015-nba-draft-data) and [here](https://data.world/jgrosz99/nba-player-data-1978-2016)), and up-to-date team data was scraped from Wikipedia.

A simple Linear Regression was used for the baseline model, but the final model used was a Random Forest Regressor. Mean Absolute Error was used as the scoring metric for interpretability.

One challenge of this project was discovering and correcting data leakage -- unexpected additional information in the training data, allowing a machine learning algorithm to make unrealistically good predictions. This leakage was coming from features such as total career minutes, total career points and total games played. These features skewed the model's predictive ability much higher because they are stats that one would only obtain at the end of a player's career (when we already know how long they played). To correct the leakage, I dropped many of the leaky columns but also used some leaky columns to feature engineer new columns (e.g. average number of games played per season).

#### Technology Used:
- Pandas
- Numpy
- Matplotlib
- Scikit-learn
- SQLite
