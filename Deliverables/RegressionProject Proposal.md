Project Proposal 

The goal is to use a regression model to evaluate what features best contribute to a baseball players Batting Average on Balls in Play. The motivation for this regression model comes from a competition put on by the MLB called 'Beat The Streak'. The premise of the competition is to chose any player in the MLB whos participating in a game that day and have them get at least one hit. If you do this 56 times in a row you win 5.6 million dollars. 

Data Sets: So far 'BASEBALL REFERENCE' has provided many player batting statistic tables. Unfortunatley the fall short of a few features id like to include(Avg Exit Velocity, Barrells to name a couple). I plan on scraping the data from BASEBALL REFERENCE using selinium and beautiful soup. And then creating an object like a dictionary to pass through the Pandas DataFrame method. 

Samples Unit of analysis: A single MLB player 

Target: BAbip 
BAbip measures how often non-home run batted balls fall for hits.

BAbip is calculated as (Hits - HomeRuns) / (AtBats - Strikeouts - HomeRuns + ScraficeFlies)
Its important to note that none of my features will be defined by the varialbes in the BAbip equation 

Possible Features: Avg Exit Velocity, Hard Hit, Barrells , Runs Created , Offensive winning percentage , Doubles, Triples. Still trying to figure the last 3 . 


The MVP should be a regression plot with 10 features(numerical and catergorical) and 1 target(numerical) with an R^2 that explains a good portion of the variation in the response variable around its mean. And hopefully has no colinearity or the model features are linearily independent. 
