# creditcard_analysis

<p align="center">
  <img src="https://github.com/user-attachments/assets/c82322bb-7f17-4dae-9dac-54c8e0be38cf" alt="Dashboard Screenshot" width="800" height="600">
</p>


The bank wants to improve their services. For instance, the bank managers have only vague idea, who is a good client (whom to offer some additional services) and who is a bad client (whom to watch carefully to minimize the bank loses). Fortunately, the bank stores data about their clients, the accounts (transactions within several months), the loans already granted, the credit cards issued The bank managers hope to improve their understanding of customers and seek specific actions to improve services. A mere application of a discovery tool will not be convincing for them.

<h1 align="center">REPORTS</h1>


## Client Classification:
The analysis involves understanding client data, transactions, loans, and credit cards.
We have surfaced some of the clients who can default. And the metrics we used for classification was how many times the balance in their accounts 
were lesser than required according to industry standards

## Economic Disparities:
There is a large variance in average salary by district, indicating significant economic disparities across different regions.
Understanding these variances can help in tailoring loan products and services to clients based on their district's economic profile.
districts like ('Hl.m. Praha', 'Mlada Boleslav', 'Plzen - mesto', 'Ostrava - mesto','Most') has really good average salaries
districts like (Chomutov,Zlin,Pardubice,Ceska Lipa) are both good in avg balance and avg salary

## Patterns in Risk:
Both the amount and duration of loans are key indicators of risk. Larger and longer loans are generally more problematic.
These patterns suggest that the bank should be cautious when approving larger and longer loans, possibly implementing stricter credit checks or requiring more collateral.
There is significant variance in average salary by district, which influences loan performance.
Key factors influencing loan success or failure are average salary, loan duration, and loan amount.


## Summary
These findings highlight the importance of careful loan approval processes, region-specific strategies, and ongoing improvements in data quality and model precision. 
By addressing these areas, the bank can enhance its understanding of client behavior, improve service offerings, and minimize financial risks.





<h1 align="center">SOME DETAILED SUMMARY</h1>

## Data Understanding
1. Business is based of operations in any regular bank such as transactions, clients, credit cards and loans.

2. Analysis of data tables relationships
3. Understanding the attribute’s “names” and their meaning
4. Understanding the attribute’s content meaning (possible values of each attribute like the range and type


## Data Preparation

Renaming attribute’s names for more meaningful keywords.
Spreadsheet “Demographic Data”
Extract implicit knowledge
Extract “birthdate” and “sex” from clients birth number
Extract client age from birth number
Eliminate incoherence provoked by empty files
District D69 had missing values that were replace by average value of all other districts
Retrieve useful information from “transaction” datasheet.
Ex.: Accounts with history of sanctions

<h1 align="center">CHARTS</h1>

#  Salary data distribution

Data shows a large variance of average salary by district.
![Screenshot 2024-07-22 123437](https://github.com/user-attachments/assets/9c7d9582-c4c0-4a58-97cf-76fafb184720)

#  Balance data distribution 
![Screenshot 2024-07-22 123524](https://github.com/user-attachments/assets/62eac367-0e8c-4641-838f-ab30f74782b5)

![Screenshot 2024-07-22 120655](https://github.com/user-attachments/assets/632c42e4-2219-403d-b86f-ee725fb658fe)
![Screenshot 2024-07-22 130126](https://github.com/user-attachments/assets/55a9abb8-ceaa-4b20-bd67-a41cf69297f1)

# Number of clients per region

Data seams equal distributed by region.
![Screenshot 2024-07-22 114932](https://github.com/user-attachments/assets/0e3dce62-a154-4b93-abe8-0de97fb0d8d2)


# Clients gender distribution

Data seems equally distributed between genders, so seems there is no bias on gender.
![Screenshot 2024-07-22 115039](https://github.com/user-attachments/assets/e38932a1-274b-4393-aa31-1027f287fcb2)


# Loan amount distribution by status

We see a pattern that loans with larger amounts tend to be more risky with clients staying with debts (type B). On the other hand, clients with smaller loans tend to finish all the loans without problems (type A).

On running contracts, we see that larger loans tend to be more suitable indebting clients (type D).
![Screenshot 2024-07-22 132221](https://github.com/user-attachments/assets/5a57b0bd-4cca-4ddc-87aa-2c9377802030)





# Loan duration distribution by status

We see a pattern that loans with longer durations tend to be more risky with clients staying with debts (type B). On the other hand, clients with smaller contract durations tend to finish all the loans without problems (type A).

On running contracts, we see that longer duration loans tend to be more suitable for indebting the clients (type D).
![Screenshot 2024-07-22 132234](https://github.com/user-attachments/assets/c2c830b5-0772-4c7c-b316-c489ab8918f8)



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


<h1 align="center">Dashboard</h1>


![Screenshot 2024-07-22 114629](https://github.com/user-attachments/assets/16db9a97-1611-4e54-9188-d62165fefc39)


![Screenshot 2024-07-22 114708](https://github.com/user-attachments/assets/d2549ec8-333a-43c2-a967-4cc5731ddd55)



























