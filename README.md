# Overview

The goal of this project was to explore, clean and analyze Reddit data (of the subreddit *unpopularopinion*) using PySpark, and to identify one or more questions of interest based on the data.

A Decision Tree Regressor was used to understand whether certain predictors were important determinants of the score (votes) of a comment, while a Random Forest Classifier was used to determine whether, given certain predictors, we can predict whether the comment would be popular/well-liked.

# Results

The first model (Decision Tree Regressor) had a Root Mean Squared Error (RSME) of approximately 51. RSME represents the square root of the variance of the residuals, and
knowledge of the data is required in order to analyze the figure correctly. Given the wide range of comment scores, an RSME of 51 is not too bad. However, it is not good either, since the lower the RSME, the better. Based on this, the independent variables chosen are not the best determinants of a comment’s score.

The second model (Random Forest Classifier) had an area under ROC of 0.6. This shows that the model does have some class separation capacity i.e. predictive power, but it is not very strong, as the closer to 1 the better. In terms of accuracy, the model predicted 58% data points correctly. This is better than chance, but not strong predictive power. Lastly, the F1 score of 0.5 for the model shows that the model is reasonable, and not completely unusable (as it would have been if the F1 score was 0). Based on this, the independent variables selected seem to be moderate or slightly above average predictors of whether the score of a comment is going to be above or
below average. 
