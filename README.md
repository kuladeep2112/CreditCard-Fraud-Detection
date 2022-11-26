# CreditCard-Fraud-Detection
Predicting a transaction is fraud or legal using machine learning 
## Problem Statement:
1) In the last years, credit and debit cards usage has significantly increased.However a non negligible part of the credit card transactions are fraudulent and billions of dollers are stolen every year throughout the world.
2) Credit card fraud detection present several characteristics that makes it a
challenging task. 
3) First, purchase behaviours and fraudster strategies may change over time, making a learnt fraud detection decision function irrelevant if not updated.This phenomenon named dataset shift (change in the distribution p(x, y)) may hinder fraud detection systems to obtain good performances.
4) Present case study,agglomarative clustering method with MCC metric is used in order to quantify the day by day dataset shift and identified calendar related time periods that show different properties grouped them into 4 clusters.<br>
5) Second,credit card transactions data suffer from a strong imbalance regarding the class labels which needs to be considered either from the classifier perspective or from the data perspective (less than 1% of the transactions are fraudulent transactions).

## Objective of casestudy:
**The objective of this casestudy is to predict the probability that an online transaction is fraudulent.**

## Dataset link
You can download data from below URL<br>
https://www.kaggle.com/competitions/ieee-fraud-detection/data

## Description of Dataset:
Throughout this work, we study a Vesta-Payment card prevention service dataset containing all the credit card transactions issued by american credit cards for a period of 6 months.<br>
Data is separated into two datasets: information about the customer identity and transaction, joined by TransactionID. Not all transactions have corresponding identity information.

* **Numerical Features - Transaction** <br><br>
    * TransactionDT:timedelta from a given reference datetime (not an actual timestamp) <br>
    * TransactionAMT: transaction payment amount in USD <br>
    * dist: distance <br>
    * C1-C14: counting, such as how many addresses are found to be associated with the payment card, etc. The actual meaning is masked.<br>
    * D1-D15: timedelta, such as days between previous transaction, etc.<br>
    * Vxxx: Vesta engineered rich features, including ranking, counting, and other entity relations.<br>
* **Categorical Features** <br><br>
    * ProductCD: product code, the product for each transaction<br>
    * card1 - card6: payment card information, such as card type, card category, issue bank, country, etc.<br>
    * addr1, addr2: address<br>
    * P_emaildomain: purchaser email domain
    * R_emaildomain: recipient email domain
    * M1 - M9: match, such as names on card and address, etc.
* **Explanation on Identity Data**
    * Variables in this table are identity information – network connection information (IP, ISP, Proxy, etc) and digital signature (UA/browser/os/version, etc) associated with transactions.
    * They're collected by Vesta’s fraud protection system and digital security partners.(The field names are masked and pairwise dictionary will not be provided for privacy protection and contract agreement).
* **Categorical Features - Identity**
    * DeviceType
    * DeviceInfo
    * id_12 - id_38
* More details about the data: https://www.kaggle.com/c/ieee-fraud-detection/discussion/101203

* We have total 4 csv files:
    * train_transaction.csv
    * train_identity.csv
    * test_transaction.csv
    * test_identification.csv
* We combine transaction,identity tables with key as TransactionID
