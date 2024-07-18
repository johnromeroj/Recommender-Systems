# Recommender-Systems

This project explores recommendation systems and provides new and experienced users with recommendations for both beer and wine.

Beer rating data was used from https://www.kaggle.com/datasets/rdoume/beerreviews.

Wine review data was used from https://www.kaggle.com/datasets/zynicide/wine-reviews.

## Collaborative Filtering 

This aspect of the project takes beer ratings from BeerAdvocate.com and uses collaborative filtering to recommend beers to users. The following notebook displays examples of using the beer recommendation system. 

https://github.com/johnromeroj/Recommender-Systems/blob/main/Collaborative-Filtering/john_romero_beer_recommender.ipynb 

### Model-Based Collaborative Filtering 

For experienced users, who have rated more than 2 beers, model-based collaborative filtering is used to predict user ratings of beers they've yet to rate based on their previous ratings of other beers in the system. Alternating Least Squares was employed using PySpark through DataBricks for this aspect of the project.

### Item-Item Memory-Based Collaborative Filtering 

For new users or users who have rated less than 3 beers, item-item memory-based collaborative filtering was used to generate recommendations. Users can identify a beer or brewery they are interested in and similar beers are recommended based on beers that have been similarly rated by experienced users. Here, k-nearest neighbors with centered-cosine similar was used to compare beers. This aspect of the project used Pyspark to preprocess data and Scikit Learn to run the KNN algorithm.


## Content Filtering 

This aspect of the project uses wine reviews from WineEnthusiast.com and uses content filtering to recommend wine to users. The following notebook shows examples of using the system.

https://github.com/johnromeroj/Recommender-Systems/blob/main/Content-Filtering/wine_knn_fitting.ipynb

Sommelier reviews of wines were used to extract representations of the wines, which were then compared to user descriptions of wines to provide wines that best match the user's description. Thus, users can recieve wine recommendations based on their description of wines they are interested in without needing high-level knowledge of the wines. Here, NLTK and Scikit Learn employed to perform text processing and cosine similarity calculations respectively.  






 
