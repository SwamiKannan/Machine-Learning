# Ensemble Model – Term Deposits

## Data:
This case is about a Portuguese bank wants to sell their term deposits. Using the collected from existing customers, build a model that will help the marketing team identify potential customers who are relatively more likely to subscribe term deposit and thus increase their hit ratio.
The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.
There are four datasets:
  1.	bank-additional-full.csv with all examples (41188) and 20 inputs, ordered by date (from May 2008 to November 2010), very close to the data analyzed in [Moro et al., 2014]
  2.	bank-additional.csv with 10% of the examples (4119), randomly selected from 1), and 20 inputs.
  3.	bank-full.csv with all examples and 17 inputs, ordered by date (older version of this dataset with less inputs).
  4.	bank.csv with 10% of the examples and 17 inputs, randomly selected from 3 (older version of this dataset with less inputs).
The smallest datasets are provided to test more computationally demanding machine learning algorithms (e.g., SVM).
The classification goal is to predict if the client will subscribe (yes/no) a term deposit (variable y).

## Data reference: 
https://archive.ics.uci.edu/ml/datasets/Bank+Marketing
## Citation: 
[Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, Elsevier, 62:22-31, June 2014
## Attributes:
### Bank Client Data:
•	Age (numeric) <br>
•	Job : type of job (categorical: 'admin.', 'blue-collar', 'entrepreneur', 'housemaid', 'management', 'retired', 'self-employed', 'services', 'student', 'technician', 'unemployed', 'unknown')<br>
•	Marital : marital status (categorical: 'divorced', 'married', 'single', 'unknown'; note: 'divorced' means divorced or widowed)<br>
•	Education (categorical: 'basic.4y', 'basic.6y', 'basic.9y', 'high.school', 'illiterate', 'professional.course', 'university.degree', 'unknown')<br>
•	Default: has credit in default? (Categorical: 'no', 'yes', 'unknown')<br>
•	Housing: has housing loan? (categorical: 'no','yes','unknown')<br>
•	Loan: has personal loan? (categorical: 'no','yes','unknown')<br>
#### # related with the last contact of the current campaign: <br>
•	Contact: contact communication type (categorical: 'cellular','telephone')<br>
•	Month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')<br>
•	Day_of_week: last contact day of the week (categorical: mon', 'tue', 'wed', 'thu', 'fri')<br>
•	Duration: last contact duration, in seconds (numeric). <br>
Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.<br>
#### # other attributes:<br>
•	Campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)<br>
•	pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)<br>
•	previous: number of contacts performed before this campaign and for this client (numeric)<br>
•	poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')<br>
#### # social and economic context attributes<br>
•	emp.var.rate: employment variation rate - quarterly indicator (numeric)<br>
•	cons.price.idx: consumer price index - monthly indicator (numeric)<br>
•	cons.conf.idx: consumer confidence index - monthly indicator (numeric)<br>
•	euribor3m: euribor 3 month rate - daily indicator (numeric)<br>
•	nr.employed: number of employees - quarterly indicator (numeric)<br>
Output variable (desired target):<br>
•	y - has the client subscribed a term deposit? (binary: 'yes','no')<br>
### Key asks:
•	Exploratory data quality report reflecting data cleanliness, uni-variate and multi-variate analysis<br>
•	Data transformation<br>
•	Build base model across multiple algorithms and assess performance<br>
•	Build the ensemble models and compare the results with the base model<br>
