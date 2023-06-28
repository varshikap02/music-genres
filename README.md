# Predicting Music Genres from Song Audio Features
This project explores a dataset from Spotify’s API that reports audio features of its songs. This dataset uses 50k randomly picked songs to predict the genre each song belongs to. 

## Data Cleaning 
Several steps were taken to deal with randomly missing data, such as mean imputation. Certain categorical feature variables were converted into numeric ones using dummy encoding. 

## Dimension Reduction 
A Principal Component Analysis (PCA) was conducted to reduce the dimensions of the dataset. 

![pca](https://github.com/varshikap02/music-genres/assets/135074696/a6a7a38c-ac73-4238-9fb8-dfe4f5078c67)

## Training 
I trained 3 classifier models - Decision Tree, Random Forest and adaBoost. I tuned hyper parameters for each of these models. I also conducted a feature importance to find that that loudness, duration and speechiness influenced genre prediction the most. After training each model, I plotted the confusion matrix, and evaluated their performance based on AUC score. 

![conf_mat](https://github.com/varshikap02/music-genres/assets/135074696/ef9362a2-ae25-47ca-9564-75989f13daea)

## Results 
I plotted the ROC curve and AUC score for each classifier. The decision tree had the best AUC score of 0.848. 

![roc](https://github.com/varshikap02/music-genres/assets/135074696/e89f9d53-8dee-4070-a1f9-bb8763e23f21)
