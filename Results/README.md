# Navigation
The folders in this directory hold the classification images of each of the models for the specified data product.
Each data product has a Train, Validation, and Testing folder where the classified images are stored. Model results are listed below

> Note: Due to computational limits of GEE accuracy results are not objective. Each pixel within the image was not used to compute the accuracy. Regions within the image were selectd to be used in the calculation of the accuracy score. 

## Results
| Validation Accuracy | | |
|----|-----|----|
| Model |	Atmosphere Validation Accuracy | Surface Reflectance Validation Accuracy |
|RF Base|	0.78|	0.74|
|RF FE|	0.73|	0.73|
|CART Base|	0.79*|	0.71|
|CART FE|	0.79|	0.88*|
|Naïve Bayes |	0.61|	0.31|
|Naïve Bayes FE|	0.37|	0.34|
|Gradient Boosting Trees Base|	0.68|	0.70|
|Gradient Boosting Trees FE|	0.67|	0.67|
|SVM Base|	0.94*|	0.72|
|SVM FE|	Error ---|	 Error ----|



> I chose the top 3 models that performed well on the validation area to test on the Kavachi area.


| Test Accuracy | | |
|--|--|--|
|Model|Atmosphere Stats| SR Stats|
|SVM Base |0.48 |----|
|CART Base|0.93|---|
|CART FE|---|.97|


