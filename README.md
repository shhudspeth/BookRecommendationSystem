# Book Recommender

These notebook contain scripts for five different recommender approaches. The first approach uses KNN and an book title API to return top ten recommendations for any given book. 

The second approach is a collaborative filtering technique using a sparse ultility matrix and KNN. And it also returns recommendations for any given book. There also includes an RSME analysis using self-coded functions (versus a library) for train, test splitting, predictions, and RMSE metrics.

The third and fourth approaches use the python library Surprise but with the data from the previous recommendation systems (aka custom data, not what is built in from Surprise). The first recommender using Surprise uses an average threshold rating of 3.5. The second Suprise recommender first averages a unique user's reviews and sets a unique threshold rating for each user-- the recommender then makes recommendations based on that unique threshold (and this approach does in fact improve ROC-AUC).  The fourth recommendation system uses PySpark and the custom data to return a RSME metric. 

Included is an API call to help return book titles and names from ISBN numbers and any one-hot encoded data, without which the recommender fails to produce meaningful information. 

KNN and a Sparse Utility matrix returns a RMSE of < 1.11 

Surprise K-Fold Baseline using Normal Predictor returns a RMSE of 1.41 

Surprise K-Fold & SVD returns a RMSE of 1.01 

Surprise K-Fold & SVD with set threshold of 3.5 has an AUC metric of 0.57 

Surprise K-Fold & SVD with user averaged threshold returns an AUC metric of 0.60 

PySpark using ALS returns RMSE of 3.6 
