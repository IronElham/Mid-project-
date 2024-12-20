# Mid-project

**Introduction:** 

Business case: As a consultant in a venture capital firm, I offer detailed analysis to entrepreneurs who are seeking for funding for their businesses. In this specific project, I have consolidated detailed analysis from Shark Tank dataset, a US TV program. This program the entrepreneurs pitching their business ideas to convince investors (Sharks) to accept the valuation of their business and negotiate a deal based on it.

For the purpose of this project, the target variable ‘got_deal’ in Shark Tank dataset is selected. This variable shows whether the entrepreneurs after pitching their ideas got the deal from the investors or not.

Problem statement: Which factors influence probability of getting deal from the investors?

Hypotheses:

H0: There is significant association between got deal and Industry.

H1: The mean of original amount asked by entrepreneur is not equal to the total_deal_amount.

H2: The mean of original_offered_equity by entrepreneur is greater than the total_deal_equity.

**Data preparation and cleaning:**

Dataframe was obtained from Kaggle data source.  The data contained 48 columns, where unnecessary columns are dropped for the purpose of this project. Data cleaning techniques used for dropping unnecessary columns, duplicates, null values, fillna, changing data types
For more specific information on cleaning data please refer to the Jupyter Notebook in the repo

**Findings:**

H0: Industry and got_deal: Fail to reject the null hypothesis, Industry does not have strong association with got_deal, where the effect size is small. 

H1: Original_amount_ask and total_deal_amount: Rejected the null hypothsis, The mean of original amount asked by entrepreneur is not equal to the total_deal_amount, where the effect size is medium. 

H2: Original_offered_equity and total_deal_equity: Fail to reject the null hypothesis, The mean of original_offered_equity by entrepreneur is less than and equal the total_deal_equity, where the effect size is small. 

**More analysis:**

1.	Multicollinear between variables total_deal_amount and investment_amount_per_shark, total_deal_equity and equity_per_shark, deal_valuation and total_deal_amount, original_offered_equity and valuation_requested , original_offered_equity and deal_valuation. 

2.	Machine learning techniques, to train feature original_offered_equity, investment_amount_per_shark, equity_per_shark , industry, State and City to predict got_deal (target variable). 

3.	Across all different ML models, all were overfitted and thus not generalizable models. In order to over the overfitting challenge, different techniques such as cross validation, removing features, regularization and ensembling has been used. As the selected features encountered high dimensionality, PCA method was the solution in reducing dimensionality and overcoming overfitting of all models. 

4.	Random forest model has the highest overall score for precision, recall, F score and accuracy. 

*For further information please refer to the Jupyther notebook and presentation on this repo.
