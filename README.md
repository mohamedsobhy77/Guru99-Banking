# Guru99 Banking Project - GTPL Bank

This is the readme.md file for the Guru99 Banking Project Software Requirements Specification.

## Introduction

The Guru99 Bank project aims to provide a net banking facility to its customers. This release will have limited features, and new functionalities will be added over time.

### Purpose

The purpose of this document is to outline the requirements for the Guru99 Banking website to be developed for Guru99 Tech. Pvt. Ltd. This document will be used by all stakeholders, including developers and testers.

### Scope

The scope of this project is limited to the testing of the features described in the succeeding sections of this document. Non-functional testing like stress, performance is beyond the scope of this project. Automation testing is also beyond the scope. Functional testing and external interfaces are in scope and need to be tested. The banking site will be compatible only with Chrome version 27 and above.

### Definitions, Acronyms, and Abbreviations

Abbreviation | Word
--- | ---
M | Manager
C | Customer

## Specific Requirements

The Guru99 Bank will have two roles: Manager and Customer. The following features/modules will be available to these two different roles:

### Manager

- New Customer
- Edit Customer
- Delete Customer
- New Account
- Edit Account
- Delete Account
- Mini Statement
- Customized Statement

### Customer

- Balance Enquiry
- Fund Transfer
- Mini Statement
- Customized Statement
- Deposit
- Withdrawal
- Change Password
- Login & Logout

## 1. Project Version 1.3

## 1.1 Introduction

This project is the first version of a banking site, which includes several modules that have been implemented for the Manager. The purpose of this version is to test the functionalities and identify any issues.

## 1.2 Modules

The following modules have been implemented for the Manager:

- New Customer
- Edit Customer
- New Account
- Edit Account
- Delete Account
- Delete Customer
- Mini Statement
- Customized Statement

## 1.3 SRS Document

For a detailed understanding of the project requirements, please refer to the Software Requirements Specification (SRS) document version 1.3 at the following link: 
- [SRS Document Version 1.3](https://docs.google.com/document/d/1wMM-7unQ77fG3IT_7ckTb4UlZm_nl6-t/edit?usp=drive_link&ouid=113231963210635393156&rtpof=true&sd=true)

## 1.4 Testing

The GitHub repository for this project contains the test cases and bug reports for version 1.3. You can find the repository at the following link: 
- [Project Version 1.3 Test Cases, Bug Reports](https://docs.google.com/spreadsheets/d/1yjRI3qu5wZexAQHpo27caqP6cDocOZH9-pAeAxLf2lE/edit?usp=drive_link).


If you're interested in testing the site, please proceed with the execution of your test cases. We welcome any feedback you may have to help improve the site's functionality. Additionally, feel free to explore the code and submit any pull requests or issues on the repository.

## 1.5 Accessing the site

The first version of the Banking Site can be accessed via the following link:
```
http://demo.guru99.com/V1/
```
However, login credentials are required to access the site.

## 1.6 Obtaining login credentials

To obtain login credentials, please follow these steps:

1. Visit ```http://demo.guru99.com/```
2. Enter your email address.
3. Login credentials for the manager will be allocated to you and displayed on the screen. Credentials will also be sent to your email address.

Sure, here's the updated Project Version 2.0 section:

## 2. Project Version 2.0

### 2.1 Introduction

This is version 2.0 of the banking site, which includes changes requested by the client to disable certain fields in the Edit Account form after submission. The development team has also fixed all bugs reported in version 1 and added the Balance Enquiry module to version 2.

### 2.2 SRS Document

For a detailed understanding of the project requirements, please refer to the Software Requirements Specification (SRS) document version 2.0 at the following link: 
- [SRS Document Version 2.0](https://docs.google.com/document/d/1ddKFnI_fEkMcHXkeP9OJ5arJlCQFHmIb/edit?usp=drive_link&ouid=113231963210635393156&rtpof=true&sd=true)

### 2.3 Testing

The GitHub repository for this project contains the test cases and bug reports for version 2.0. You can find the repository at the following links: 
- [Project Version 2.0 Test Cases, Bug Reports](https://docs.google.com/spreadsheets/d/1yjRI3qu5wZexAQHpo27caqP6cDocOZH9-pAeAxLf2lE/edit?usp=drive_link)

If you have previously run test cases on version 1.0 of the banking site, you can now re-run your failed test cases on version 2.0. The development team has fixed all reported bugs, and the site should now be functioning as expected.

### 2.4 Accessing the site

The second version of the Banking Site can be accessed via the following link: 
```
http://demo.guru99.com/V2/
```
Please use the login credentials generated for version 1 to access the site.

### 2.5 Obtaining login credentials

To obtain login credentials, please follow these steps:

1. Visit ```http://demo.guru99.com/```
2. Enter your email address.
3. Login credentials for the manager will be allocated to you and displayed on the screen. Credentials will also be sent to your email address.

## 3. Project Version 3.0

### 3.1 Introduction

Refer the Changelog to determine the changes made in the test cases as per the SRS v2.
Refer the SRS_v3. The client now wants a Webservice created. Create test cases to check this webservice.

### 3.2 SRS Document

For a detailed understanding of the project requirements, please refer to the Software Requirements Specification (SRS) document version 3.0 at the following link:

[SRS Document Version 3.0](https://docs.google.com/document/d/1jjXGZrk2v5VfUvbCN_t6W_oH3nbbVNJg/edit?usp=drive_link&ouid=113231963210635393156&rtpof=true&sd=true)

### 3.3 Software Interfaces

The bank will provide a mobile app wherein a customer can:

- See mini statement for his account.
- See balance enquiry for his account.

Two web service calls are created so the mobile app can connect to the net banking database and sink data. Details as below.

### 3.4 Mini Statement

Get last 5 transaction details from server

Output Format: JSON

API call category: User

API Request:

http://demo.guru99.com/V3/sinkministatement.php?CUSTOMER_ID=cust123&PASSWORD=cust123&Account_No=123

Input Parameter:

Type | Description
--- | ---
CustomerID | Mandatory. User’s customer id.
Password | Mandatory. User’s password.
AccountNumber | Mandatory. Account Number for which statements are required.

Response:

```
{
   "result":{
      "Statements":[
         {
            "Transaction ID":123,
            "Amount":"10000",
            "Transaction Type":"W",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-10-01",
            "Description":"Self"
         },
         {
            "Transaction ID":142,
            "Amount":"10000",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-10-09",
            "Description":"Self"
         },
         {
            "Transaction ID":1111,
            "Amount":"700",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-15-09",
            "Description":"Self"
         },
         {
            "Transaction ID":148,
            "Amount":"7000",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-17-09",
            "Description":"Self"
         },
         {
            "Transaction ID":158,
            "Amount":"5500",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-18-09",
            "Description":"Self"
         }
      ]
   },
   "message":{
      "ErrorCode":0,
      "ErrorMsg":"error message"
   }
}
```

### 3.5 Balance Enquiry

Get Balance from User Account

Output Format: JSON

API call category: User

API Request:

http://demo.guru99.com/V3/sinkbalanceenquiry.php?CUSTOMER_ID=cust123&PASSWORD=cust123&Account_No=123

Input Parameter:

Type | Description
--- | ---
CustomerID | Mandatory. User’s customer id.
Password | Mandatory. User’s password.
AccountNumber | Optional. If user enters Account_No then display balance for account associate with Account_No. If user not enters Account_No then display balance for all account associated with it.

Response:

```
{
   "result":{
      "Balance":[
         {
            "ACCOUNT_NO":123,
            "ACCOUNT_TYPE":"Saving",
            "BALANCE":"10000"
         },
         {
            "ACCOUNT_NO":256,
            "ACCOUNT_TYPE":"Current",
            "BALANCE":"50000"
         },
         {
            "ACCOUNT_NO":298,
            "ACCOUNT_TYPE":"saving",
            "BALANCE":"20"
         }
      ]
   },
   "message":{
      "ErrorCode":0,
      "ErrorMsg":"error message"
   }
}
```

Error Code Table:

Error Code # | Error Code Message
--- | ---
0 | Success
1 | NoData
2 | Connection Issue
3 | Login Credentials Incorrect

### 3.6 Testing

The GitHub repository for this project contains the test cases and bug reports for version 3.0. You can find the repository at the following links:

- [Project Version 3.0 Test Cases, Bug Reports](https://docs.google.com/spreadsheets/d/1yjRI3qu5wZexAQHpo27caqP6cDocOZH9-pAeAxLf2lE/edit?usp=drive_link)



## 4. Project Version 4.0

### 4.1 Introduction

There is another change request and the SRS is updated. Refer the SRS_v4. Change the System Test Plan as the new SRS.

### 4.2 SRS Document

Please refer to the Software Requirements Specification (SRS) document version 4.0 at the following link:

[SRS Document Version 4.0](https://docs.google.com/document/d/1W88ScpaWG6p1GFkAb1ghJKpsL2_rZrjh/edit?usp=drive_link&ouid=113231963210635393156&rtpof=true&sd=true)

### 4.3 Software Interfaces

The bank will provide a mobile app wherein a customer can:

- See mini statement for his account.
- See balance enquiry for his account.

Two web service calls are created so the mobile app can connect to the net banking database and sink data. Details as below.

### 4.4 Mini Statement

Get last 5 transaction details from server

Output Format: JSON

API call category: User

API Request:

http://demo.guru99.com/V4/sinkministatement.php?CUSTOMER_ID=68195&PASSWORD=1234!&Account_No=1

Input Parameter:

Type | Description
--- | ---
CustomerID | Mandatory. User’s customer id.
Password | Mandatory. User’s password.
AccountNumber | Mandatory. Account Number for which statements are required.

Response:

```
{
   "result":{
      "Statements":[
         {
            "Transaction ID":123,
            "Amount":"10000",
            "Transaction Type":"W",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-10-01",
            "Description":"Self"
         },
         {
            "Transaction ID":142,
            "Amount":"10000",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-10-09",
            "Description":"Self"
         },
         {
            "Transaction ID":1111,
            "Amount":"700",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-15-09",
            "Description":"Self"
         },
         {
            "Transaction ID":148,
            "Amount":"7000",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-17-09",
            "Description":"Self"
         },
         {
            "Transaction ID":158,
            "Amount":"5500",
            "Transaction Type":"d",
            "ACCOUNT_NO":"123",
            "Date of Transaction":"2013-18-09",
            "Description":"Self"
         }
      ]
   },
   "message":{
      "ErrorCode":0,
      "ErrorMsg":"error message"
   }
}
```

### 4.5 Balance Enquiry

Get Balance from User Account

Output Format: JSON

API call category: User

API Request:

http://demo.guru99.com/V4/sinkbalanceenquiry.php?CUSTOMER_ID=68195&PASSWORD=1234!&Account_No=

Input Parameter:

Type | Description
--- | ---
CustomerID | Mandatory. User’s customer id.
Password | Mandatory. User’s password.
AccountNumber | Optional. If user enters Account_No then display balance for account associated with Account_No. If user does not enter Account_No then display balance for all accounts associated with it.

Response:

```
{
   "result":{
      "Balance":[
         {
            "ACCOUNT_NO":123,
            "ACCOUNT_TYPE":"Saving",
            "BALANCE":"10000"
         },
         {
            "ACCOUNT_NO":256,
            "ACCOUNT_TYPE":"Current",
            "BALANCE":"50000"
         },
         {
            "ACCOUNT_NO":298,
            "ACCOUNT_TYPE":"saving",
            "BALANCE":"20"
         }
      ]
   },
   "message":{
      "ErrorCode":0,
      "ErrorMsg":"error message"
   }
}
```

Error Code Table:

Error Code # | Error Code Message
--- | ---
0 | Success
1 | NoData
2 | Connection Issue
3 | Login Credentials Incorrect

The final release of the website is now available at http://demo.guru99.com/V4/.

Login Credentials:
- Manage Id: use the id given to you since version 1
- Customer Id: use the id you created in version 3. You can also create new ids in version 4.

### 4.6 Testing

The GitHub repository for this project contains the test cases and bug reports for version 4.0. You can find the repository at the following links:

- [Project Version 4.0 Test Cases, Bug Reports](https://docs.google.com/spreadsheets/d/1yjRI3qu5wZexAQHpo27caqP6cDocOZH9-pAeAxLf2lE/edit?usp=drive_link)


