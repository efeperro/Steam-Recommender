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

Nonpersonalized Recommendation Engine 

Collaborative Filtering Engine

Content-Based Recommendation Engine

Conclusion

Bibliography
https://amplitude.com/blog/recommendation-engine
https://www.iteratorshq.com/blog/an-introduction-recommender-systems-9-easy-examples
https://www.androidauthority.com/what-is-steam-3254981/ 
https://analyticsindiamag.com/cold-start-problem-in-recommender-systems-and-its-mitigation-techniques/?utm_content=cmp-true 
Steam games recommendation engine

