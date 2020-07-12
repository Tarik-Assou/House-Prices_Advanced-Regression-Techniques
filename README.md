# House-Prices_Advanced-Regression-Techniques

![Scores of models](https://user-images.githubusercontent.com/67377289/87241549-a7204c80-c424-11ea-8937-7b22c9c6984f.PNG)

## The Goal
- Each row in the dataset describes the characteristics of a house.
- My goal is to predict the SalePrice, given these features.
- The models are evaluated on the Root-Mean-Squared-Error (RMSE) between the log of the SalePrice predicted by our model, and the log of the actual SalePrice. Converting RMSE errors to a log scale ensures that errors in predicting expensive houses and cheap houses will affect our score equally.
## Key features of the model training process in this kernel:
1. Cross Validation: Using 12-fold cross-validation.
2. Models: On each run of cross-validation I fit 7 models (ridge, svr, gradient boosting, random forest, xgboost, lightgbm regressors).
3. Stacking: In addition, I trained a meta StackingCVRegressor optimized using xgboost.
4. Blending: All models trained will overfit the training data to varying degrees. Therefore, to make final predictions, I blended their predictions together to get more robust predictions.
