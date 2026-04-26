# Boston Housing Price Analysis
A supervised machine learning case study predicting median home values in the Boston area. Dataset from Harrison & Rubinfeld (1978) contains 506 observations, 13 socioeconomic and structural predictors.

**Models Compared:**
- Linear Regression (with stepwise AIC variable selection)
- Regression Tree (pruned via cross-validated CP)
- k-Nearest Neighbor (scaled, optimal k selected by validation RMSE)
- Random Forests (500 trees, mtry ≈ 4)
- Boosting (GBM, 10,000 trees, λ = 0.01)
- Generalized Additive Model (GAM with mixed smooth/linear terms)
- Neural Network (single hidden layer, 5 nodes, scaled inputs)

**Key Findings:**      
- Neural Networks, Boosting, and Random Forests achieved the lowest out-of-sample prediction error.    
- lstat (% lower-status population) and rm (average rooms per dwelling) were the strongest predictors across all models.    
- GAM revealed significant nonlinear relationships that the linear model could not capture.    
- The dataset's $50K censoring cap on home values creates a known artifact in the upper tail of predictions.

**Tools**    
R · ggplot2 · randomForest · gbm · mgcv · neuralnet · rpart    
**Course**    
BANA 7047 Data Mining II - University of Cincinnati, M.S. in Business Analytics
