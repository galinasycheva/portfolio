# Churn rate study

This study was conducted for the network of gym centers, which develops a strategy for interacting with clients based on analytical data.

The purpose of the study is to analyze the customer churn rate and prepare an action plan for retaining clients.

**Research objectives:**

- learn to predict the probability of churn (at the level of the next month) for each client;
- form typical portraits of clients: identify several of the most striking groups and characterize their main properties;
- analyze the main features that most strongly affect churn;
- formulate the main conclusions and develop recommendations for improving the quality of work with clients:
- identify target groups of clients;
- propose measures to reduce churn;
- determine other features of interaction with clients.

The data contains data for the month before the churn and the fact of churn for a certain month. The data set includes the following fields: customer data for the month preceding the churn fact check and information based on the visit log, purchases and information about the current status of the client's membership:

## Summary

For exploratory data analysis, I looked at the histograms of the distribution of features for users who left the gym and those who stayed, and also looked at the Pearson and Spearman correlations. I made several conclusions:

the distribution of the proximity indicator among those who left and those who stayed is approximately the same
among those who left, there are fewer employees - partner companies of the gym than among those who stayed
the average age of those who left is less than among those who stayed
the highest correlation is for the Churn with the features Avg_class_frequency_total, Lifetime, Age and Month_to_end_contract
Based on the data, I conclude that when working with outgoing clients, it is necessary to pay attention primarily to those who come often and whose membership is ending soon - perhaps it is worth offering them favorable terms for renewal of the membership.

To conduct the prediction analysis, the data was divided into a validation and training sample in a ratio of 80 to 20. Two models were used in the analysis - logistic regression and random forest.
In both cases, the accuracy, precision and recall metrics showed good results - all indicators are greater than 0.8, which is close to one and means that the models correctly, completely and accurately predict more than 80% of responses.

When constructing the dendrogram, I identified 5 clusters.
The pairwise graphs show that users who often visit the gym and use other services of the gym overlap strongly with each other. It is also clear that old users and users who often visit the gym also overlap.
