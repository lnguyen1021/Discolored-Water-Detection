# Navigation
The scripts for each model can be found in the folders corresponding to the data product either atmosphere or surface reflectance bands. 
Scripts are named with the following nominclature: dataProduct_trainingOrTestingScript_modelName

### Modeling
GEE has various Machine Learning algorithms that can be directly called from GEE.  [The methods anddocumentation for differnent methods can be found here.](https://developers.google.com/earth-engine/guides/classification)

For this project several models were created utilizing two different data products (top of atmosphere reflectance bands and surface reflectance bands).
1. Classification and Regression Trees (CART) <!--data is split into different feature groups and then subset based on trying to create a homogenous values along the dependent variable (decision trees) -->
2. Random Forest <!-- ensembling method of decision trees by bootstrap sampling the data and splitting into different groups of predictor groups and trying to split the group to create homogenous groups -->
3. Gradient Boosted Trees <!-- similar to random forest but instead of creating multiple trees in parallel, GBT does this sequentially creating weak learners and combining to create a strong learner. the weak learners 'learn' the mistake of the prior model and tries to reduce the residual of the previous tree -->
4. Naive Bayes <!--the independent feature model, that is, the naïve Bayes probability model. The naïve Bayes classifier combines this model with a decision rule. The common rule is to pick the hypothesis that is most probable; this is known as the maximum a posteriori or MAP decision rule. -->
5. Support Vector Machines <!-- tries to seperate each class along a plane and maximizing the distance between each class. -->

Additionally, a few feeatures were engineered from band calculations. Each of the model listed above was created twice. One a base model with no additional features and a second model that included the additional features listed below. <!--https://github.com/sentinel-hub/custom-scripts/blob/master/sentinel-2/se2waq/script.js-->
1. Chloraphyll a concentrations
2. Density of cyanobacteria
3. Turbidity
4. Colored dissolved organix matter
5. Dissolved organic carbon

<hr> 
