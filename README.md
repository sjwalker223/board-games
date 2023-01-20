# Board Game Explorer
In my free time, I love to go to my local board game cafe and play board games with my friends. But the cafe has SO MANY games; how can we even begin to choose what to play next?

We know several games that we enjoy already - so what if we could ask an assistant to recommend similar games that we might also enjoy?

The aim of this project is twofold:
1. Create the Board Game Explorer - a recommendation app that will take a game that the user likes and recommend 5 similar games that they could try next. Try it yourself at https://boardgame-explorer.onrender.com/.

2. Explore what categories of board games are amongst the most popular, which publishers produce the most popular games, and what makes a game more likely to be highly rated.

## The approach
The data for this project comes from http://www.boardgameatlas.com. This data contains a variety of information about the top 500 board games on this website.

The recommendation system applies a KNN model to this data to identify the games with the highest degree of similarity to one another. The recommendations are then presented in an interactive Dash app.

## The files
`BoardGame_Explorer` contains the code for all the steps of the recommendation system, from obtaining the data from an API, through data cleanup, EDA and model generation, to outputting the recommendations in a Dash app.

`Games_Meta`,`Games_df` and `knn_indices_df` are outputs of the Explorer, which are used in downstream analysis and in the online Dash app.

Note: the Dash app deploys locally. To view an online version of this app, check out https://boardgame-explorer.onrender.com/.

## Key insights
- There are a range of game genres amongst the top 500 games, with most genres only containing a few games. However, a small number of genres have many games in the top 500, with card games being the top category.
- Most publishers only have a few (1-3) games in the top 500, and the majority of games are from one of these "minor" publishers. However, a small number of publishers have an outsized number of games in the top 500 - Fantasy Flight Games being the biggest of these, with 34 games in the top 500.
- There is a weak correlation between playtime and average user rating - so longer (and potentially more complex) games are somewhat more likely to have a higher rating than shorter games.
- Using data from BoardGameAtlas allows us to provide recommendations that make sense!