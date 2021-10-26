Problem Statement: 

We made a regression model in order to predict the heisman trophy winner for a given year in order to understand the relationship between player and team data and heisman winners.

A succinct formulation of the question your analysis seeks to answer:

The Heisman Trophy is the penultimate award for NCAA college football that supposedly is awarded to the best football player of the year. Which players are in the running is a common topic of discussion in the sports media and online forums. This project seeks to use data related to player statistics, specifically passing, rushing and receiving data and college team data to predict which College football player is mostly likely going to win the Heisman Trophy


Description of Data: 

The data we used for this project was web scraped from the website Sports Reference. Because defensive players are rarely represented in the Heisamn top ten, we decided to exclude them from our data set. Additionally, we decided to focus on only the last twenty years of data (2000 - 2020) both due to time constraints and also because comparing years more than 20 years apart might affect the model due to changes in the game of college football. On Sports Reference, player data is divided into three sections: top players for rushing, top players for receiving and top players for passing. The amount of players in each section varies by year, usually between 100-500 players per section. We used a request to scrape the data from the website and then created a function to parse through the html and formulate it into a dataframe. In addition to player data we also scraped team win-loss records per year. Heisman trophy winners are elected through a voting process with the top ten players being displayed on the website. We scraped this data as our target variable. We concated all data  until we had one data set per year and a data set with all the years. Some player names had a star next to them indicating if their data included postseason games so we removed the star with the replace function. We also converted all the sata types to numeric data as it was originally all object data type. 


Software Requirements:

For web scraping we used requests, lxml, beautiful soup and pandas 

For modeling we used, pandas, tensorflow, keras, matplotlib, sklearn, and numpy


Conclusion/Future Analysis:

Overall the models performed better than expected. Although we weren’t able to account for player personalities and team politics, the player stats were able to carry the models to some degree. We originally sought to utilize classification but ultimately chose regression as our predictor due to data limitations. AdaBoost, Neural Networks, and Random Forest were our best performing ML models. 

We were only able to do minimal optimization and analysis of the features. This would improve our model scores. This can be achieved through grid search. Adding a running back and wide receiver rating would also potentially improve our predictions. Lastly, as a part of follow on analysis we hope to create a dashboard tool that generates our predictions with player stat inputs. 


Dictionary: 


|Code|
||Workbook Name|Folder|Description|
|---|---|---|---|
|Passing|code|Code book for web scraping player passing data| 
|Rushing|code|Code book for web scraping player rushing data|
|Receiving|code|Code book for web scraping player passing data|
|Standing|code|Code book for web scraping team standing data|
|Voting|code|Code book for web scraping Heisman voting data|
|Year|code|Code book for concating yearly data|
|Linear Regression|code|Code book for modeling with Linear Regression|
|AdaB RanFor KNN|code|Code book for modeling with KNN, Ada boost and K nearest neighbors|
|Neural Networks|code|Code book for modeling with Neural Networks|


|Data|
||Workbook Name|Folder|Description|
|---|---|---|---|
|Passing|Data|Compilation of passing data pertaining to player, team, and Heisman stats|
|Rushing|Data|Compilation of rushing data pertaining to player, team, and Heisman stats|
|Receiving|Data|Compilation of receiving data pertaining to player, team, and Heisman stats|
|Standing|Data|Compilation of data pertaining to College Football team win/loss records|
|Heisman Voting|Data|Compilation of data pertaining to Heisman candidate votes|
|Year|Data|Compilation of data that includes annual player, team, and Heisman stats|

