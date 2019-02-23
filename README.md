# Czech Bank's Financial Data Analysis. Moving from gut feeling to data-driven decisions.
Data analysis of a real Czech bank. 

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

Data from a real Czech bank. From 1999.
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


### Run
In a terminal or command window, navigate to the top-level project directory finding_donors/ (that contains this README) and run one of the following commands:

ipython notebook Czech-banking-customer-trans-analysis.ipynb
or

jupyter notebook fCzech-banking-customer-trans-analysis.ipynb
This will open the iPython Notebook software and project file in your browser.

Overview
The notebook covers supervised learning techniques applied on data collected for the U.S. census to help CharityML (a fictitious charity organization) identify people most likely to donate. Data was analyzed, series of transformations and pre-processing steps applied to manipulate the data into a workable format. Linear SVC, Decision Tree Classifier and Gradient Boosting Classifier (GBC) sklearn models were evaluated so to find best solution. Based on the evaluation results sklearn GBC was selected as the most promising. The model was optimized using sklearn grid search. Additionally features importance was analyzed, the importance of each feature when making predictions based on the chosen algorithm.

Features

age: Age
workclass: Working Class (Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked)
education_level: Level of Education (Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool)
education-num: Number of educational years completed
marital-status: Marital status (Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse)
occupation: Work Occupation (Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces)
relationship: Relationship Status (Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried)
race: Race (White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black)
sex: Sex (Female, Male)
capital-gain: Monetary Capital Gains
capital-loss: Monetary Capital Losses
hours-per-week: Average Hours Per Week Worked
native-country: Native Country (United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands)
Target Variable

income: Income Class (<=50K, >50K)
Results
Optimized model of Gradient Boosting Classifier is giving accurracy as 0.8689 and F-score (beta 0.5) as 0.7483 on test set.
