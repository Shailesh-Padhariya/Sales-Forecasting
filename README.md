Sales Forecasting Using Machine Learning

Project Overview:

This project focuses on predicting sales using various machine learning models. The dataset includes key sales indicators such as product details, store attributes, and promotional factors. The goal is to develop an accurate predictive model by comparing multiple regression techniques.

Exploratory Data Analysis (EDA):

Checked for missing values and filled them using mean/mode where necessary.
Created new attributes such as New_Item_Type and Outlet_Years for better insights.
Standardized categorical variables using Label Encoding and One-Hot Encoding.
Applied log transformation to normalize skewed distributions.
Visualized feature distributions using histograms, count plots, and correlation heatmaps.

Machine Learning Models Used
Multiple regression models were implemented and evaluated based on their predictive performance. The following models were tested:

1- Linear Regression
Accuracy of Test data
R2_Score: 0.7136391970550767
Accuracy of Training data
R2_Score: 0.7232624990443841
Accuracy of Complete data
R2_Score: 0.7203110558484953


2- Ridge Regressor:
Accuracy of Test data
R2_Score: 0.7132086988032402
Accuracy of Training data
R2_Score: 0.7230806625087245
Accuracy of Complete data
R2_Score: 0.7200528916859534

3- Lasso Regressor:
Accuracy of Test data
R2_Score: 0.2538352830427828
Accuracy of Training data
R2_Score: 0.26227683517122646
Accuracy of Complete data
R2_Score: 0.2596923551013075

4- Decision Tree:
R2_Score: 0.45102637369632226
Accuracy of Training data
R2_Score: 1.0
Accuracy of Complete data
R2_Score: 0.8314868609091011

5- RandomForestRegressor
Accuracy of Test data
R2_Score: 0.6948330517333665
Accuracy of Training data
R2_Score: 0.9595054320208344
Accuracy of Complete data
R2_Score: 0.8782618743334945


6- ExtraTreesRegressor
Accuracy of Test data
R2_Score: 0.6794029668532795
Accuracy of Training data
R2_Score: 1.0
Accuracy of Complete data
R2_Score: 0.901589420966285

7- LGBMRegressor

Accuracy of Test data
R2_Score: 0.7222631749410455
Accuracy of Training data
R2_Score: 0.8159406776859842
Accuracy of Complete data
R2_Score: 0.7871870802560543

Randomized search Cv was used for hyper-parameter tuning for following models:
1- Random Forest 
Accuracy of Test data
R2_Score: 0.7123927087467647
Accuracy of Training data
R2_Score: 0.8282664975938355
Accuracy of Complete data
R2_Score: 0.7926994076664702

2- LGBMRegressor
Accuracy of Test data
R2_Score: 0.7378840825312187
Accuracy of Training data
R2_Score: 0.7474040017170538
Accuracy of Complete data
R2_Score: 0.7444840723233541

3- XGBRegressor
Accuracy
Accuracy of Test data
R2_Score: 0.7391462915552081
Accuracy of Training data
R2_Score: 0.7472569668211906
Accuracy of Complete data
R2_Score: 0.7447696207847848

Insights from Model Performance Results
1. Best Performing Models
LGBMRegressor (Regular & Tuned) achieved the highest performance with an overall R² score of 0.787 (regular) and 0.744 (tuned).
XGBRegressor (Tuned) performed well with an overall R² score of 0.744, slightly below LGBM.
Random Forest (Tuned) improved its test R² score to 0.712, making it a strong contender.

2. Overfitting Models
Decision Tree (Regular) had an R² score of 1.0 on training data but 0.451 on test data, indicating extreme overfitting.
Random Forest (Regular) and Extra Trees both had 1.0 training scores, but their test scores were lower (0.694 and 0.679, respectively), indicating they are learning the training data too well but struggling to generalize.

3. Poor Performing Models
Lasso Regression had the lowest performance, with an R² score of 0.253 (test) and 0.259 (overall). This suggests that it is unable to capture enough complexity in the data.
Ridge Regression performed similarly to Linear Regression, with both achieving an R² score of around 0.713 on test data, showing slight improvements in regularization.

4. Effect of Hyperparameter Tuning
Randomized Search CV helped improve models:
Random Forest (Tuned) increased its test R² to 0.712 (vs. 0.694 in the regular version).
LGBM (Tuned) slightly improved test performance (0.737) but had a drop in training accuracy, suggesting a better balance.
XGBoost (Tuned) performed similarly to LGBM with a test R² of 0.739, showing that boosting models work well on this dataset.


Final Recommendation
LGBM or XGBoost should be used for final deployment since they provide the best balance of accuracy and generalization.
Random Forest (Tuned) is a strong alternative but may require additional tuning.
Decision Trees should be avoided in their current form due to severe overfitting.

Conclusion
This project successfully applied machine learning techniques to forecast sales. The LGBM model provided the best results, making it the preferred choice for future sales predictions. Further improvements can be made by optimizing features and testing advanced models.
