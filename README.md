# ML-Credit-Risk-Modeling

**Codebasics ML Course Development of Credit Risk Model for Lauki Finance**

## Project Overview:
Lauki Finance, a Non-Banking Financial Company (NBFC) based in India, 
is partnering with AtliQ AI, a leading AI service provider, to develop a sophisticated credit risk 
model. This model will include a credit scorecard that categorizes loan applications into Poor, 
Average, Good, and Excellent categories, based on criteria similar to the CIBIL scoring system.

## Data
* Customer data

| **Feature**                     | **Description**                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------|
| `cust_id`                        | Unique identifier for each customer.                                                                     |
| `age`                            | Age of the customer, typically used as a predictor of credit behavior and financial responsibility.       |
| `gender`                         | Gender of the customer, often included for demographic analysis (though not directly impacting credit).    |
| `marital_status`                 | Marital status of the customer, which may affect household income and financial stability.                |
| `employment_status`              | Employment status (e.g., employed, unemployed, self-employed), critical for assessing financial stability. |
| `income`                         | Annual income of the customer, a key factor in determining the ability to repay credit.                   |
| `number_of_dependants`           | Number of dependents relying on the customer’s income, which could impact disposable income.              |
| `residence_type`                 | Type of residence (e.g., owned, rented), which could indicate financial commitments.                     |
| `years_at_current_address`       | Length of time the customer has lived at their current address, often used to assess stability.           |
| `city`                           | City of residence, may be used for regional analysis or to compare living costs.                         |
| `state`                          | State of residence, often used to apply different regional rules or credit policies.                     |
| `zipcode`                        | Zip code of the residence, useful for geographical segmentation and regional risk analysis.              |

* Loan data

| **Feature**                        | **Description**                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `loan_id`                           | Unique identifier for each loan application or account.                                                          |
| `cust_id`                           | Unique identifier for each customer, linking the loan to the customer’s profile.                                 |
| `loan_purpose`                      | The stated purpose of the loan (e.g., personal, business, home, auto).                                           |
| `loan_type`                         | The type of loan (e.g., secured, unsecured, fixed, variable).                                                    |
| `sanction_amount`                   | The loan amount that was approved for the customer.                                                              |
| `loan_amount`                       | The actual amount disbursed to the customer after sanctioning.                                                   |
| `processing_fee`                    | Fees charged to the customer for processing the loan application.                                                |
| `gst`                               | Goods and Services Tax applied to the processing fee or other loan-related charges.                              |
| `net_disbursement`                  | The total amount disbursed to the customer after deductions, such as fees.                                       |
| `loan_tenure_months`                | The length of time (in months) over which the loan must be repaid.                                               |
| `principal_outstanding`             | The remaining principal amount of the loan that has yet to be repaid.                                            |
| `bank_balance_at_application`       | The customer’s bank balance at the time of the loan application, possibly used for financial assessment.          |
| `disbursal_date`                    | The date when the loan was disbursed to the customer.                                                            |
| `installment_start_dt`              | The date on which the loan installment payments are scheduled to begin.                                          |
| `default`                           | Indicates whether the loan has defaulted (yes/no), used to track risk and customer repayment behavior.            |

* Bureau data
  
| **Feature**                    | **Description**                                                                                          |
|--------------------------------|----------------------------------------------------------------------------------------------------------|
| `cust_id`                      | Unique identifier for each customer, used to link bureau data to specific customer records.              |
| `number_of_open_accounts`      | The number of credit accounts currently open in the customer's name.                                     |
| `number_of_closed_accounts`    | The number of credit accounts that have been closed in the customer's history.                           |
| `total_loan_months`            | Total months of loan exposure or credit history for the customer.                                        |
| `delinquent_months`            | The number of months where the customer had overdue payments.                                            |
| `total_dpd`                    | Total days past due (DPD) across all credit accounts, reflecting overall payment behavior.               |
| `enquiry_count`                | The number of inquiries or credit checks made by creditors on the customer's credit report.              |
| `credit_utilization_ratio`     | The ratio of current credit balance to the credit limit, indicating how much available credit is used.   |

## Model Explanation:
* Best model: Linear Regression with 96% accuracy, 98% AUC and 96% Gini

## Building Apps:
![image](https://github.com/user-attachments/assets/b38ac51e-bff3-43b2-bb55-aed9bed3da62)

- The `artifacts` contains model, scaler, features, and colume to be scaled. 

## Deploying the Application:
You can access the deployed application here: [Streamlit App](https://ml-credit-risk-modeling-app.streamlit.app/)
