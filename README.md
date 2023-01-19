# Customer_Churn_Factors
 
# Project Description

Telco is a world renowned telecommunications company that provides phone, internet, and streaming services to their customers. As technology evolves, so does the company's business model. In order to stay up to date on current market trends and ensuring the satisfaction of our customers, it is necessary to analyze customer data. As you will soon see, there may be some factors that influence customer churn that can be remediated to keep customers with the company.  Different models are ran to determine what factors have the greatest influence on customer churn and the results will hopefully spark discussion on how to decrease customer churn.

# Project Goal
 
* Discover factors that lead to customer churn.
* Use factors to develop a machine learning model to predict whether a customer will churn or not.
* Churn is defined by a customer leaving the company or canceling services
* This information can be used to improve customer satisfaction by improving services that may lead to customer churn.
 
# Initial Thoughts
 
My initial hypothesis is there will be multiple factors that influence customer churn with the most being total cost. I also think that the type of contract a customer has and internet_service type will also play a role.
 
# The Plan
 
* Aquire data from Sequal Server
 
* Prepare data
   * Create Engineered columns from existing data
       * gender
       * online_security
       * internet_service_type
       * contract_type
       * monthly_charges
       * total_charges
       * churn
 
* Explore data in search of drivers of churn
   * Answer the following initial questions
       * How often does churn occur?
       * Do total_charges affect churn?
       * Do monthly_charges affect churn?
       * Does contract_type affect churn?
       * Does having online_security affect churn?
       * Does a customer's internet service type affect churn?
      
* Develop a Model to predict if a customer will churn
   * Use factors identified in explore to build predictive models of different types
   * Evaluate models on train and validate data
   * Select the best model based on highest accuracy
   * Evaluate the best model on test data
 
* Draw conclusions
 
# Data Dictionary

| Feature | Definition |
|:--------|:-----------|
|online_security| True or False, states whether or not customer has online_security|
|churn (target)| True or False, if True, this means that the customer cancelled their services|
|monthly_charges| How much money in USD a customer pays per month|
|total_charges| How much money in USD a customer has paid over the course of their contract(s)|
|contract_type| The length of a customer's contract before they can cancel without penalties|
|internet_service_type| Indicates which internet service a customer has: DSL, Fiber Optic, or No Internet
|scaled_total| Scaled value for total charges per customer
|scaled_monthly| scaled value for monthly charges per customer

# Steps to Reproduce
1) Clone this repo.
2) Acquire the data from sql database
3) Put the data in the file containing the cloned repo.
4) Run notebook.
 
# Takeaways and Conclusions
* "Internet service type" and "online security" were each found to be factors of "churn"
    * The influence appears strong
* Monthly charges appears to have influence on churn
    * the spread of the distribution indicates that the influence is weak
* Contract type can may influence churn based on visuals
* Having online security also affects churn as shown in our visuals
* These are enough features to create a model that can predict customer churn
 
# Recommendations
* Consider lowering price of Fiber Optic and increase customers with online_security
* Use Logistic Regression model to predict whether or not a customer is going to churn and have marketing team target these customers
* Accquire more demographic data from customers
