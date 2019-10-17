#Book Recommender

These notebook contain scripts for five different recommender approaches. The first approach is KNN and using an book title API, returns top ten recommendations for any given book. The second approach is a collaborative filtering technique using a sparse matrix. The third and fourth uses custom data and the python library Surprise. The first recommender using Surprise uses an average threshold rating of three. The second Suprise recommender first averages a unique user's reviews and sets a unique threshold rating for each user-- the recommender then makes recommendations based on that unique threshold (and this approach does in fact improve ROC-AUC).  The fourth uses PySpark and the custom data to return a RSME metric. 

Included is an API call to help return book titles and names from ISBN numbers and any one-hot encoded data, without which the recommender fails to produce meaningful information. 
