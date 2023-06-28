# Predicting Music Genres from Song Audio Features
This project explores a dataset from Spotify’s API that reports audio features of its songs. This dataset uses 50k randomly picked songs to predict the genre each song belongs to. 

## Data Cleaning 
Several steps were taken to deal with randomly missing data, such as mean imputation. Certain categorical feature variables were converted into numeric ones using dummy encoding. 

## Dimension Reduction 
A Principal Component Analysis (PCA) was conducted to reduce the dimensions of the dataset. 

![pca](https://github.com/varshikap02/music-genres/assets/135074696/90b45de7-b5af-42c1-b4ad-8813ea55dccf)

## Training 
I trained 3 classifier models - Decision Tree, Random Forest and adaBoost. I tuned hyper parameters for each of these models. I also conducted a feature importance to find that that loudness, duration and speechiness influenced genre prediction the most. After training each model, I plotted the confusion matrix, and evaluated their performance based on AUC score. 

![conf](https://github.com/varshikap02/music-genres/assets/135074696/8e239ced-44ca-438d-91b2-5551213a844c)

From the confusion matrix, we observe that Classical music had the highest number of correctly predicted labels than any other genre, while Alternative music had the lowest number of correct predictions. Several Alternative genre songs were incorrectly classified as Rock music, highlighting the similarities between those genres. 

## Results 
I plotted the ROC curve and AUC score for each classifier. The decision tree had the best AUC score of 0.848. 

![roc](https://github.com/varshikap02/music-genres/assets/135074696/9695a837-5a91-4d42-ab16-4ffdf55c3763)

The ROC curve is consistent with the results presented by the confusion matrix - the classical genre is the easiest to predict, while alternative is the toughest. 
