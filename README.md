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
      
* Develop a Model to predict if a chess game will end in an upset
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
 
# Steps to Reproduce
1) Clone this repo.
2) Acquire the data from sql database
3) Put the data in the file containing the cloned repo.
4) Run notebook.
 
# Takeaways and Conclusions
* Upsets occur in 1/3 of games
* In games where the lower rated player moves first there is a 4% greater chance of an upset
* Games that are rated have a 3% higher chance of an upset
* Games with a "quick" time control (30 min or less) have about a 1 in 3 chance of upset
* Games with a "slow" time control (60 min or more) have about a 1 in 5 chance of upset
* The mean rating of players in a game is not a driver of upsets
* The difference in player rating is a driver of upsets
* A player's choice of opening is a driver of upsets, however its influence is complicated and I would need more time to discover what role it plays
 
# Recommendations
* To increase the skill intensity of a game add to the length of time players are able to consider their moves
* Based on the data longer time controls make it less likely for a less skilled player to beat a more skilled player
