# Collaborative-Filtering-based-Recommendation-System-for-Movies-
This project implements a movie recommendation system using collaborative filtering techniques. The goal is to accurately predict movie ratings for users and provide personalized recommendations.

Approach
The recommender system utilizes both memory-based and model-based collaborative filtering:

Memory-based: Computes cosine similarity between users after filling in missing ratings.
Model-based: Performs matrix factorization with SVD on the user-rating matrix to discover latent factors.
To fill in missing ratings, an unsupervised clustering approach is used:

Movies are clustered by genre using K-means, based on principal components of movie genres.
For each user, their average rating for each cluster is computed.
Missing user ratings for a movie are imputed with the user's average rating for that movie's cluster.
This imputation method provides more specificity than a simple row-mean.

Results
The memory-based approach achieved lower error than the model-based SVD approach. Both methods produced low RMSE and MAE, indicating the efficacy of the proposed clustering and imputation technique.

Conclusion
The results demonstrate the feasibility of using a hybrid approach with clustering and collaborative filtering for robust and accurate movie recommendations. There are opportunities to explore improvements to the imputation methodology.

References
Katarya, R. (2018). Movie recommender system with metaheuristic artificial bee. Neural Computing and Applications, 30(6), 1983-1990.

Pornwattanavichai, A., Jirachanchaisiri, P., Kitsupapaisan, J., Maneeroj, S., & Thipakorn, B. (2020). Enhanced Tweet Hybrid Recommender System Using Unsupervised Topic Modeling and Matrix Factorization-Based Neural Network. In Supervised and Unsupervised Learning for Data Science (pp. 121-143). Springer.

Afoudi, Y., Lazaar, M., & Al Achhab, M. (2021). Intelligent recommender system based on unsupervised machine learning and demographic attributes. Simulation Modelling Practice and Theory, 107, 102198.
