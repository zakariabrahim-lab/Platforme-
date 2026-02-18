# Loan Management Platform

## Overview
This Loan Management Platform is designed to streamline the management of loans, making it easier to track and manage borrowing and lending processes. This document provides comprehensive information about the platform, including its features, authentication, GP list, data structure, installation steps, formulas used, objectives, and alert rules.

## Features
- **User Authentication**: Secure login and registration process for users.
- **Loan Tracking**: Keep track of all loans and their statuses.
- **Payment Scheduling**: Automated scheduling for loan repayments.
- **Reporting**: Generate detailed reports on loan activities.
- **Alerts and Notifications**: Sends alerts for recent loan activities and important deadlines.

## Authentication
The system uses JWT (JSON Web Tokens) for authentication. Users must register to obtain an access token, which is required for accessing protected routes.

### Registration
- Endpoint: `/api/register`
- Method: `POST`
- Required fields: `username`, `password`, `email`

### Login
- Endpoint: `/api/login`
- Method: `POST`
- Required fields: `username`, `password`

## GP List
The General Practitioner (GP) list consists of authorized users who can access the platform. The GP roles are defined as follows:
1. Admin: Full access to all features.
2. Manager: Can manage loans and view reports.
3. User: Can apply for loans and view personal loan status.

## Data Structure
The platform uses the following data structure for managing loans:
- **Loan**:
  - `loan_id`: Unique identifier for the loan
  - `user_id`: Identifier for the user who took the loan
  - `amount`: Amount borrowed
  - `interest_rate`: Interest applicable on the loan
  - `start_date`: Date when the loan was issued
  - `end_date`: Expiry date of the loan
  - `status`: Current status of the loan (active, closed)

## Installation
To install the Loan Management Platform, follow these steps:
1. Clone the repository:
   ```
   git clone https://github.com/zakariabrahim-lab/Platforme-
   ```
2. Navigate to the project directory:
   ```
   cd Platforme-
   ```
3. Install the dependencies:
   ```
   npm install
   ```
4. Configure the environment variables according to `.env.example`.
5. Run the application:
   ```
   npm start
   ```

## Formulas
The following formulas are used within the platform:
- **Interest Calculation**:  
  \[ 
  	ext{Interest} = 	ext{Principal} \times \text{Rate} \times \text{Time} 
  \]
- **Total Amount Payable**:  
  \[ 
  	ext{Total} = 	ext{Principal} + 	ext{Interest} 
  \]

## Objectives
- Provide a user-friendly interface for managing loans.
- Ensure secure handling of user data and authentication.
- Automate the loan reporting process.

## Alert Rules
The platform has various alert rules to keep users informed about their loans:
- **Payment Due Alert**: Notifies the user 7 days before the payment is due.
- **Loan Approval Alert**: Informs the user once their loan has been approved.
- **Loan Expiry Alert**: Alerts users when their loan is about to expire.

## Conclusion
This documentation serves as a comprehensive guide to using the Loan Management Platform. For further queries, consider reaching out to the development team.