# Predicting Football Match Results

This project builds a machine learning model that can be used to predict professional soccer games. 

The model uses Logistic Regression, built from the given data from all the matches. 

All the explanation and wall-through steps are included in the ipython notebook called football_prediction.jpynd. 
There are two python files that are used by this notebook:

* features: Turns raw statistics into features that get fed into the machine learning model. These features combine information from team_attribute and player_attributes for each of the matchs. 
* models: Helper methods for cleaning the data and building and running the logistic regression model.

## Data Description: 
+ match: information of the match betwen 2 football teams: home_team and away_team
    - date: date of the match
    - home/away_team_api_id: id of home/away team
    - home/away_player_(1..11): id of players from home/away team
    - home/away_player_X/Y(1..11): starting lineup (in coordinate X, Y)
    - goal, shoton, ..., corner, possession: match progress 
    - B365H, B365D, ..., BSD, BSA: bet rate
+ team, player: information of the team and players
+ team_attributes: team stats
    - team_api_id: team id
    - date: date of the stats collection
    - buildUpPlaySpeed, ..., defenceDefenderLineClass: team stats
+ player_attributest: players stats
    - player_api_id: player id
    - date: date of the stats collection
    - overall_rating, ..., gk_reflexes: player stats
+ country, league: name of country and league

## Tasks:
+ Analyse and explain whether the following factor impacts the final result of the match:
    + Team Profile
    + Players Profile
    + Starting Players from both teams
    + Historical matches between the two teams
    + Other factors
+ Build a predictive model using the above analysis to predict the outcome of the game (which team is more likely to win)
+ Choose the appropriate evaluation metrics for the task