# Regression

Predicting a MLB Players BABIB

Jimmy Gardner

Abstract

The goal of this project was to attempt to model a players Batting Average On Balls In Play(BABIP) using a regression model. This was in an attempt to isolate the particualr batting statistics that contribute most to a players BABIP. And was further motivated by attempting to isolate features that would make a particular player more likely to get a hit in any particular game. Chosing players with a high BABIP is good, but understanding what features drive BABIP is almost as important when chosing a player to get a hit.

Design

As outlined in the abstract above , the goal of this project was to come away with certain features that would contribute to a players likelihood of getting a hit. The design is centered around a simple linear regression model, as well as an attempt to add complexity through a polynomial regression model of degree 2.

Algorithms

Feature Engineering

Most features were chosen based off contextual knowledge and intuition and were validated or disproven through running multiple iterations of a simple linear regression model

An attempt at engineering a defensive metric was made. Each team has a unique UZR. UZR puts a run value to defense , attempting to quantify how many runs a team saved or gave up through fielding prowess. Engineering this feature turned out to be very labor intensive, because each player plays a unique schedule( except for those that play on the same team), so each player has a unique advantage or disadvantage based on the quality of defense they played throughout the year, represented by AVGUZR. Unfortuntley after engineering this feature a simple pair plot showed little to no correlation between BABIP and AVGUZR

Chosing a feature that would incorporate a players speed. The more infield hits a player has the more likely he is a fast player that puts above average pressure on the defense. So depending on your speed , this could hurt or enhance your BABIP.

Models

A simple linear regression model was used and ended up producing the best results. A second degree polynomial model was also used, but ended up producing a much lower R^2. The backbone of the linear regression model is Ordinary Least Squares. 

Most of my features were in similar numerical intervals, so there wasnt much need for scaling. I ran a scaled ridged regression, and came up with an almost identical R^2

Simple linear Regression Results

R^2 on validation: 0.461 R^2 on test: 0.468 MEAN SQUARED ERROR(Test): 0.000668 MEAN ABSOLUTE ERROR(Test): 0.01878

Polynomial regression Results

Degree 2 polynomial regression val R^2: 0.425 Degree 2 polynomial test R^2: 0.437

Standard Scaler Using Ridge

Ridge Regression Validation R^2: 0.461 Ridge Regression Test R^2: 0.460

Tools

For my tools I incorporated Ptyhon and a few relevant librarie: Sklearn for modeling and Matplotlib and Seaborn for plotting. I used Beautiful Soup and Selinium to scrape my data.

Communication

Five minute power point presentation and slides from that presentation .
