# Steam Recommender

## Background
Recommendation engines are data filtering predictive analysis systems that utilize user data, statistics, and machine learning to predict which products, services, content, or listings a user will prefer. Such engines are crucial for online businesses and services aiming to maximize profit by offering personalization. The overall goal of recommendation engines is to suggest content that the user will be interested in, as opposed to providing random products. In this project, a number of recommendation engines have been constructed and applied to a dataset containing information about Steam gamers. Steam is a platform for distributing video games online that also possesses community forums It was developed by Valve, the creators of famous video games like Half-Life, Counter Strike and Left4Dead. The dataset originally contained the following variables: 

#### User ID (numeric)
A collection of unique user ID  

#### Name of the Steam Game (string)
The name of each game played by the user, unordered

#### Purchase (string)
A variable containing two values: purchase, or play 

#### Hours that the user played each game
Values equal to 1.0 represent a user purchasing a game

#### An extra variable containing only 0’s, holding no information


### Cold Start Recommendation Engine
In the realm of recommendation engines, programmers must confront an initial setback known as the “cold start problem”. The cold start problem occurs when it has insufficient data, and it cannot form any relation between items and users to create a recommendation. The cold start problem can be applied to both users and products. All recommendation engine programmers must invent a creative solution for their cold start that is appropriate for the task at hand. The cold start solution for a Steam game recommender revolves around new users who have no gaming activity. It involves the recommendation of the overall most popular games towards new users, in hopes that one will draw their interest which will in turn generate crucial user data. A simple recommender that finds the all games that have an average rating of at least 3, then, the top ten games that have the highest total gaming hours by users will be selected. This simple, but robust, solution will ensure that the user will have a variety of games to select from that are beloved among the community.

### Nonpersonalized Recommendation Engine 
A non-personalized recommendation engine provides general recommendations that are not tailored to the individual preferences of a user. In the context of Steam, our non-personalized recommendation engine takes into account three variables that are converted into a rating matrix:

* 'User ID'
* 'Game Title'
* 'Rating (1 - 5)'

This rating matrix is then fed into a recommendation engine using the "Popular" method. This engine simply recommends the most popular games. Additionally, this engine had a true positive rate of 71%, meaning that it recommended correctly about 7 out of 10 games that it should have recommended.

### Collaborative Filtering Engine
A user-based collaborative filtering engine in the context of a video game vending service would be finding similar users and recommending them non-mutual video games in their respective libraries.  In order to provide more information to our recommendation engine, the two datasets previously were merged.

Our engine functioned as such:
* The variables Game Title, User ID, Hours Played, Ratings, Genres and Release Year were taken into account. 
* A rating matrix was made, and then split into train and test sets.
* The recommender model was made under the "UBCF" model, and predictions were run

RMSE in recommendation engines is a measure of the average magnitude of errors in the predictions of the engine
After much trial and error, the best RMSE score returned was a 68.03

### Content-Based Recommendation Engine
Content-Based Recommender suggests games to users based on their preferences and the features of the games.  With the following models, we aimed to predict the variables 'Ratings' and 'HoursPlayed'. 

#### Tested ML Models: 
* Linear Regression
* Random Forest
* XGBoost
* Neural Network.

#### Performance Metrics:
* 'HoursPlayed' prediction models show overall better performance on MSE and MAE.
* For the target variable 'Rating', the best performing model out of all of them was Linear Regression - which had the least R-squared value along with the lowest MSE and MAE.
* For the target variable 'HoursPlayed', the best performing model was our Neural Netowork, which was the only model that got a positive R-squared value.


### Conclusion
#### Top Performers
* Neural Networks for predicting "HoursPlayed".
* XGBoost for predicting "HoursPlayed".
* Linear Regression for predicting "Ratings".


### Contributors

* Sindi Bejko
* Fabian Perez
* Alex Svenburg
* Nathan Zeidel

