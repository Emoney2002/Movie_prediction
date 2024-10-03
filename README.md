# Movie_prediction
Movie Recommendation System using K-Nearest Neighbors (KNN)
This project builds a recommendation system for movies based on user ratings. I apply K-Nearest Neighbors (KNN) as a collaborative filtering method to suggest movies to users based on the preferences of their nearest neighbors (users with similar tastes). The project involves both Exploratory Data Analysis (EDA) and a KNN-based recommendation model to predict movie ratings and generate recommendations.


Project Overview

The goal of this project is to build a movie recommendation system using K-Nearest Neighbors (KNN), where user preferences are used to recommend movies to similar users. The project starts with data exploration and visualization, followed by building a collaborative filtering-based recommendation model.

Dataset
The dataset consists of two files:

movies.csv: Contains movie information with the following columns:

movieId: Unique identifier for each movie.

title: The title of the movie.

genres: Movie genres, separated by a pipe (|).

ratings.csv: Contains user ratings for movies with the following columns:


userId: Unique identifier for each user.

movieId: Unique identifier for the rated movie.

rating: The rating given by the user (from 0.5 to 5.0).

timestamp: The timestamp when the rating was given.

Exploratory Data Analysis (EDA)
I performed EDA on the movies and ratings datasets to gain insights:

Rating Distribution: Most ratings are concentrated around 3 to 5 stars.

Genre Popularity: The most common genres are Drama, Comedy, Thriller, and Romance.

Basic Statistics: I calculated summary statistics like mean and standard deviation of user ratings and checked for missing values (none were found).

Recommendation Model
We implemented a K-Nearest Neighbors (KNN) model to build a collaborative filtering-based recommendation system.

Steps:
Utility Matrix:I created a utility matrix where rows represent users and columns represent movies, with the matrix values being the user ratings.

KNN Model:I applied KNN using cosine similarity to find similar users (neighbors) for a given user.

Recommendation: Based on the nearest neighbors' preferences, I recommended movies that the target user has not yet rated.

Key Features:

Cosine Similarity: I used cosine similarity to measure the closeness between users.

Top-K Neighbors: The model identified the top 5 nearest neighbors for each user to generate recommendations.

Evaluation
We evaluated the performance of the KNN model using Root Mean Squared Error (RMSE). The RMSE measures the error between the predicted and actual ratings for movies that a user has already rated.

RMSE:
RMSE = 1.70: This means the model's predicted ratings deviate by an average of 1.7 stars from the actual ratings, indicating reasonable performance but with room for improvement.

Results

Based on the KNN model, here are some recommended movies for a sample user (User 0):

Batman Forever (1995)
Dumb & Dumber (1994)
The Lion King (1994)
The Rock (1996)
Indiana Jones and the Last Crusade (1989)
The Truman Show (1998)
Good Will Hunting (1997)
X-Men (2000)
Memento (2000)
Pirates of the Caribbean: The Curse of the Black Pearl (2003)

Future Improvements
Hyperparameter Tuning: Experiment with different values for K in KNN, and try various similarity metrics like Pearson correlation or Euclidean distance.

Matrix Factorization: Implement more advanced collaborative filtering techniques like Singular Value Decomposition (SVD) or Alternating Least Squares (ALS).

Content-Based Filtering: Incorporate movie features such as genres, directors, or release year for hybrid recommendations.

Precision & Recall: Implement metrics such as precision and recall to measure the effectiveness of recommendations.
