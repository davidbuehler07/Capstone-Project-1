# Capstone Project 1 PlayerUnknown's Battlegrounds - Using Player Data to Find the Best Way to Win in PUBG

![pu_battlegrounds-2060x1159](https://user-images.githubusercontent.com/52009110/69174724-33a58580-0ab7-11ea-89dc-c7ec3977b982.jpg)

## Data Problem

PlayerUnknown's Battlegrounds (PUBG) is an extremely popular video game on the PC launcher Steam, with millions of copies downloaded all over the world. Kaggle, the data science competition website, posted a challenge: to predict players win place percentage based off a number of in-game factors, including kills, kill streaks, distance walked/swam/driven, kill place, and many others. The question posed by the competition: "What's the best strategy to win in PUBG? Should you sit in one spot and hide your way to victory, or do you need to be the top shot?"

## Who's Interested?

There could be a couple groups of people who would be interested in this sort of problem. Firstly the developers of the game at PUBG Corporation, a subsidiary of Bluehole. The developers would want to understand how players are playing the game, and whether they enjoy how the game is being played. Generally a more fun and player engaging way to play PUBG is the run-n-gun play style. Pick up a gun and some ammo and go look for people to kill. Compared to a different play style that's focused more around camping and staying in one spot and letting people come to you. The community generally finds this to be a boring play style, and the developers would certainly want to know the best strategy to win in a given game, and make balancing changes based off the findings.

Another group that could be interested is the playerbase themselves, especially the more hardcore players who are always looking to improve and win games. If they know and understand the best ways to win, and how to get those wins, they would be interested in what the anaylsis has to say.

## The Data Set

The original data set, found ![here on Kaggle](https://www.kaggle.com/c/pubg-finish-placement-prediction), consisted of 4.45 million rows of data points, each representing a different player in a game they were in. Also consists of 29 columns, each describing an in-game statstic that's relevant to the problem at hand, including:

1. Kills, kill streaks, and kill place
2. Ride distance, swim distance, and walk distance
3. Heals, boosts and other staying-alive metrics
4. The target: win place percentage

I decided to only look at the solos game mode, so it's one person against 99 others and it's a fight to be the last one standing. This removed the extra factor of having people be in teams, as well as being my personal favorite game type. It gives the true battle royale experience.

Modeling the data set was done with supervised regression models, including Linear Regression, Lasso and Ridge Regression, Random Forest Regression and XGBoost for some extra practice. We were specifically looking at how important each variable was to the final prediction, or feature analysis, and did so through the use of coefficients of importance to each model 

## Findings

* After looking at 5 different models, the best way to win in PUBG is to keep moving and not camp
* Linear and Ridge Regression had a top coefficient of road kills
* Lasso Regression had a top coefficient of weapons acquired
* Random Forest Regression and XGBoost both had a top coefficient of walk distance
  * Kill place coming in second for Random Forest and third for XGBoost

