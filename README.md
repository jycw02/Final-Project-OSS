# Final-Project-OSS
Movie Recommender System

This is my end project for Open Source Software.

##Dependencies
numpy (http://www.numpy.org/)
scipy (https://www.scipy.org/)


This project is a movie based recommender. The system computes similarity scores for movies based on their cast, overview and genres. 
The dataset is from MovieLens: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata 

Here you can see what the dataset normally looks like:
![example dataset](https://user-images.githubusercontent.com/113161516/206757242-1b8aa43e-2ca0-4fca-98d9-50e1a73d58db.PNG)


The data needs to be presented in a good structure, to find the right words that fit the recommender. So, from this metadata, I found out the five most important elements (e.g the five most important actors).

The first step was to import the data. After that i merged and cleaned the dataset (remove dashes, reduce datavolume). Then i created vectors (Term Frequency-Inverse Document Frequency). This technique places more importance on rare words instead of stopwords, like "a". This helps improve the recommendation accuracy (Term Frequency-Inverse Document Frequency finds how many times a word appears)
This eventually provides a matrix where the columns give an overview of the vocab that appear in the movie, and show how the improtance of words.

Text should be preprocessed and converted. So, I performed dimension reduction. With the help of the matrix, I computed a score that shows the similarity of a movie. 
- I used sklearn linear_kernel() for finding out the similarity score.
- I used CountVectorizer to count how many times a word comes.


HOW IT WORKS:
Based on the input in the system, the system will recommend five movies that are most similar.
![example](https://user-images.githubusercontent.com/113161516/206758165-215299ef-bb68-4b97-9ea9-9b29c22852eb.PNG)

Here you can see the highlighted part is where the movie name will be inserted. After that you run the system, and the movies will be recommended. See the following picture of a series of examples

![examples](https://user-images.githubusercontent.com/113161516/206758341-57584b5d-3abe-4af0-8eb6-55e8eeff3fdb.PNG)

