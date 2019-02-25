# Czech Bank's Financial Data Analysis. Moving from gut feeling to data-driven decisions.
Data analysis of a real Czech bank. 

### Motivation
The notebook contains overview of following questions and even more than that: 
-  Customers age and gender population overview.
-  Can we identify most attractive districts in Czech Republic for future marketing campaigns? Criteria: higher number of inhabitants, prominent average salary and low level of clients representation.
-  Credit department efficiency overview within country: which districts are giving mostly “good” or “bad” loans?
-  Bank’s funds inflows and outflows analysis. Does the bank face negative cash flow rarely or often? Is there any patterns for funds outlay?

### Install
This project requires Python 3.x and the following Python libraries installed:

1. NumPy
2. Pandas
3. Matplotlib
4. Seborn 
5. Plotly 
6. Collections 

You will also need to have software installed to run and execute an iPython Notebook

### Code
Code is provided in the Czech-banking-customer-trans-analysis.ipynb notebook file. 

### Data 

Data from a real Czech bank. From 1999. Reported period 1993 - 1998.
The data about the clients and their accounts consist of following relations:
-  relation account (4500 objects in the file ACCOUNT.CSV) - each record describes static characteristics of an account,
-  relation client (5369 objects in the file CLIENT.CSV) - each record describes characteristics of a client,
-  relation disposition (5369 objects in the file DISP.CSV) - each record relates together a client with an account i.e. this relation describes the rights of clients to operate accounts,
-  relation permanent order (6471 objects in the file ORDER.CSV) - each record describes characteristics of a payment order,
-  relation transaction (1056320 objects in the file TRANS.CSV) - each record describes one transaction on an account,
-  relation loan (682 objects in the file LOAN.CSV) - each record describes a loan granted for a given account,
-  relation credit card (892 objects in the file CARD.CSV) - each record describes a credit card issued to an account,
-  relation demographic data (77 objects in the file DISTRICT.CSV) - each record describes demographic characteristics of a district.
Each account has both static characteristics (e.g. date of creation, address of the branch) given in relation "account" and dynamic characteristics (e.g. payments debited or credited, balances) given in relations "permanent order" and "transaction". Relation "client" describes characteristics of persons who can manipulate with the accounts. One client can have more accounts, more clients can manipulate with single account; clients and accounts are related together in relation "disposition". Relations "loan" and "credit card" describe some services which the bank offers to its clients; more credit cards can be issued to an account, at most one loan can be granted for an account. Relation "demographic data" gives some publicly available information about the districts (e.g. the unemployment rate); additional information about the clients can be deduced from this.

Data map 

![data map.gif](https://view.dwcontent.com/file_view/lpetrocelli/czech-financial-dataset-real-anonymized-transactions/data%20map.gif?auth=eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJwcm9kLXVzZXItY2xpZW50OnRhbGdhdCIsImlzcyI6ImFnZW50OnRhbGdhdDo6ZGRkNjczOGItMjE3My00ZjJmLWJlMzctOTIxNTU2MzgyYWNhIiwiaWF0IjoxNTQ5MjcyMzc5LCJyb2xlIjpbInVzZXIiLCJ1c2VyX2FwaV9hZG1pbiIsInVzZXJfYXBpX3JlYWQiLCJ1c2VyX2FwaV93cml0ZSJdLCJnZW5lcmFsLXB1cnBvc2UiOmZhbHNlLCJ1cmwiOiJlYjA3MWQ2ODY4N2Y3NmY4NzM0ZGUzM2MzZjk3MTIzNDgxOWYwZTBjIn0.1bYEPgFwBlTGWf40nJzSdDyDJbi7YYqPJ-K-yeYOZ7SSc8rkMSc-ubQFbRoFZiQrhvoHpgzyq_mvON_Xo7MQBA)

### Data dictionary 

List of datasets and data dicitonary can be found in Data dictionary.pdf

### Run
In a terminal or command window, navigate to the top-level project directory czech-banking-fin-analysis/ (that contains this README) and run one of the following commands:

ipython notebook Czech-banking-customer-trans-analysis.ipynb
or

jupyter notebook fCzech-banking-customer-trans-analysis.ipynb
This will open the iPython Notebook software and project file in your browser.

### Acknowledgement

I am thankful to @lpetrocelli for real Czech bank's data shared at https://data.world/lpetrocelli/czech-financial-dataset-real-anonymized-transactions and to TSilveira for data visualization examples: https://www.kaggle.com/tsilveira/applying-heatmaps-for-categorical-data-analysis  

### License 
Code released under the MIT License. 
