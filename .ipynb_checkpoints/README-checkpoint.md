# Board Game Explorer
In my free time, I love to go to my local board game cafe and play board games with my friends. But the cafe has SO MANY games; how can we even begin to choose what to play next?

We know several games that we enjoy already - so what if we could ask an assistant to recommend similar games that we might also enjoy?

The aim of this project is twofold:
1. Create the Board Game Explorer - a recommendation app that will take a game that the user likes and recommend 5 similar games that they could try next. Try it yourself at https://boardgame-explorer.onrender.com/.

2. Generate Board Game Analytics that a board game company could use to decide: 1) who to market their new game to; and 2) what genre of game to produce next, based on current game trends.

## The approach
The data for this project comes from http://www.boardgameatlas.com. This data contains a variety of information about the top 500 board games on this website.

The recommendation system applies a KNN model to this data to identify the games with the highest degree of similarity to one another. The recommendations are then presented in an interactive Dash app.

## The files
`BoardGame_Explorer` contains the code for all the steps of the recommendation system, from obtaining the data from an API, through data cleanup, EDA and model generation, to outputting the recommendations in a Dash app.

`Games_Meta`,`Games_df` and `knn_indices_df` are outputs of the Explorer, which are used in downstream analysis and in the online Dash app.

Note: the Dash app deploys locally. To view an online version of this app, check out https://boardgame-explorer.onrender.com/.