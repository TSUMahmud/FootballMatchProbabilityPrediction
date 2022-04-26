# FootballMatchProbabilityPrediction

The processed data are used in these files. They are available at: https://drive.google.com/drive/folders/1HGLgWDYjgfJ3o34XNrlyfCR3wWqWb0lQ?usp=sharing

* Logistic Regression - We used logistic regression at first. We used the LogisticRegression classifier provided by sklearn with solver 'lbfgs' and 1000 maximum iteration as parameter. We used 5 fold cross validation to generate 5 models and average the probability of them.
* Decision Tree - We applied grid search to find best parameters for the Decision Tree. From that, we found max\_depth 7 and criterion 'gini' is the best parameter to build a decision tree.
* Bagging - We applied grid search to find best model and number of estimator for the begging classifier. From that, we found decision tree with depth 2 and 300 estimators are the best parameter to build a bagging classifier in this dataset.
* Random Forest - We used random forest with 300 and 500 estimators.
* AdaBoost - We used AdaBoost with decision tree with depth 1 and 2 as well as 300 and 500 estimators.
* xGBoost - We created 5 models of xGBoost using 5 fold cross validation data and average the probability of the models to generate the output.
* LightGBM - We created 5 models of LightGBM using 5 fold cross validation data and average the probability of the models to generate the output. We built LightGBM models using boosting type "gbdt", which is the gradient based decision tree, metric multi\_logloss, learning rate 0.02/0.05 and maximum depth of 5.
* Neural Network - We created a neural network of two dense layers with and without a dropout layer after both layers.
* LSTM - We created LSTM models of different combination of two bidirectional LSTM layers along with a dropout layer each, a maxpooling and flatten layer before the output layer.
* Ensemble - Here we used the prediction of our best two performer xGBoost and LightGBM to create an ensemble model. We tried different weight scheme to calculate the weighted average of those two models.
