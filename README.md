# Spotify Mining

I worked on this project for a seminar at my university. 
The task was to analyze music tracks with some ML-approaches to understand better, which features have an influence on the popularity and which expression on this featrues leads to a higher popularity.
The data comes from Spotify provided via Kaggle https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks (*New Link, old data is not available anymore*)

**Note that the paper is in german.**

## Used ML-Approaches

Usage of Scikit-Learn and XGBoost
- Linear Regression
- kNN
- Decicion Tree
- Random Forest
- Boosted Tree (XGBoost)

## Explainable ML
I used the SHAP framwork (https://github.com/slundberg/shap) to get a better understanding of the results of the ML-Tools

## Key takeaways
First this plot shows the development of the music features over the years. One can clearly see the rise of electronic music starting in the 1950's. in the 80's explicit music emerges because of the popularity of Rap music. 
![features_year](https://user-images.githubusercontent.com/55655975/194762706-254a7a3e-2abf-4a4b-b42f-de138a094364.png)

The correlation matrix show's that year, acousticness have a high impact on the popularity. Energy, instrumentalness, loudness and explicit have also a mior impact.
The year has the highes impact, because spotify weights a recent listening higher.
![Correlation_matrix_features](https://user-images.githubusercontent.com/55655975/194761996-4bff485f-1792-427a-bd28-d956143c3a74.png)

Here the importend features are plotted to show, which value is related to a higher popularity.
![features_popularity](https://user-images.githubusercontent.com/55655975/194762582-ec2a85b5-1ce8-4eed-9f1a-866824c8538a.png)

With the SHAP-Values we can explore better wich value of the features are better for a higher popularity.
![SHAP_impact_on_output](https://user-images.githubusercontent.com/55655975/194762959-2ecd82a6-6be0-4abd-8669-99a664d7fea1.png)

The framework also allows us to pick a singel song and tell us wich feature is to high or low to improve the predicted poularity
![SHAP_strahl](https://user-images.githubusercontent.com/55655975/194763148-0f8cb40c-4e34-4f88-bff9-722c10e60c88.png)

