# creditcard_analysis
The bank wants to improve their services. For instance, the bank managers have only vague idea, who is a good client (whom to offer some additional services) and who is a bad client (whom to watch carefully to minimize the bank loses). Fortunately, the bank stores data about their clients, the accounts (transactions within several months), the loans already granted, the credit cards issued The bank managers hope to improve their understanding of customers and seek specific actions to improve services. A mere application of a discovery tool will not be convincing for them.



# Data Understanding
1. Business is based of operations in any regular bank such as transactions, clients, credit cards and loans.

2. Analysis of data tables relationships
3. Understanding the attribute’s “names” and their meaning
4. Understanding the attribute’s content meaning (possible values of each attribute like the range and type


# Data Preparation

Renaming attribute’s names for more meaningful keywords.
Spreadsheet “Demographic Data”
Extract implicit knowledge
Extract “birthdate” and “sex” from clients birth number
Extract client age from birth number
Eliminate incoherence provoked by empty files
District D69 had missing values that were replace by average value of all other districts
Retrieve useful information from “transaction” datasheet.
Ex.: Accounts with history of sanctions

#  Salary data distribution

Data shows a large variance of average salary by district.

# Number of clients per region

Data seams equal distributed by region.

# Clients gender distribution

Data seems equally distributed between genders, so seems there is no bias on gender.


# Loan amount distribution by status

We see a pattern that loans with larger amounts tend to be more risky with clients staying with debts (type B). On the other hand, clients with smaller loans tend to finish all the loans without problems (type A).

On running contracts, we see that larger loans tend to be more suitable indebting clients (type D).

# Loan duration distribution by status

We see a pattern that loans with longer durations tend to be more risky with clients staying with debts (type B). On the other hand, clients with smaller contract durations tend to finish all the loans without problems (type A).

On running contracts, we see that longer duration loans tend to be more suitable for indebting the clients (type D).

# Data problems and applied solutions

We had a small dataset of finished loans 
Around 234 finished loans (loans with status A or B)
Around 448 active loans (loans with status C or D)
Recurrent overfitting the model.
Modification of (pre)pruning parameters.
Ignoring of irrelevant attributes.
We opted for not using any date related field because that would make the model unsuitable for future predictions.
We opted to not use gender as a decision variable too.
There isn’t a good distribution of loans by status.
The majority of the current loans are of type C and finished loans of type A, difficulting the prediction of bad indicators for loans.

# Conclusion

We come to the conclusion that the most influencing attributes for loans success or failure are “average salary” of clients demographic data, “duration” and “amount” of the loans.
But in general this is a unsatisfactory result with really low precision.













