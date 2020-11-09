# Credit-card-linear-regression

<h2>Objective </h2>
The bank conducted survey of 5000 customers andcollected data. Objective is to understand what's driving the total spend(Primary Credit Card + Secondary Credit Card) of the customer. Given the factors, predict credit limit for the new applicants.

In statistics, linear regression is a linear approach to modeling the relationship between a scalar response or dependent variable and one or more explanatory variables or independent variables. In our case the  dependent variables are "cardspent" and "card2spent".

(**ASSUMPTIONS**)  
- No Multicollinearity
- No Heteroscedasticity 
- No Auto correlation
- Residual should be normally distributed

The feature selection is done with the help of correlation matrix, f_regression method to infer the relation of each feature with the dependent variables. 

VIF (variance inflation method) is used to infer the relation of the independent variable with each other.

The model can be further improved by keeping the R squared high and the difference between R squared and the adjusted R squared as low as possible otherwise it will indicate multicollinearity in our model. 

<h2>First Linear Model Summary :</h2>

![](LR-Model-1.png)

**Assumption** voilated :- Residual is not normally distributed.
There were some Influential Points that where affecting the parameter of the Model

<h2>Final Linear Model Summary :</h2>

![](LR-Model-2.png)

After Removing those Influential Points and satisfying the **Assumption**.

<h2>Conclusion :</h2>
Linear regression is used to train the model. The following features were selected to train the model i.e. these features are driving the total spend of the customer is mentioned below:

<br>

**Feature that affecting total spend of Customers**

- age : Age in years 
- carcatvalue : Primary vehicle price category
- card2 : Secondary credit card
- card2type : Designation of secondary credit card
- card : Primary credit card
- cardtype : Designation of primary credit card
- debtinc : Debt to income ratio (x100)
- lncreddebt : Log-credit card debt
- lninc : Log-income
- othdebt : Other debt in thousands

