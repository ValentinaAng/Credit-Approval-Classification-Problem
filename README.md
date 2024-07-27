# Project Title:
Credit Approval Classification 


# Table of Content:
1. Data Loading
2. Data Analysis
3. Exploratory Data Analysis
4. Data Splitting
5. Data Preprocessing
6. Model Training and Evaluation
7. Results
8. Final Conclusion


# Project Description
This dataset provides information that helps us identify patterns and develop a model to determine whether a credit application will be approved. 
The dataset will be uploaded in CSV format and includes the following features:


| Field Name              | Order | Type (Format) | Description                                                        |
|-------------------------|-------|---------------|--------------------------------------------------------------------|
| checking_status         | 1     | string (default) | Status of existing checking account, in Deutsche Mark.             |
| duration                | 2     | number (default) | Duration in months                                                 |
| credit_history          | 3     | string (default) | Credit history (credits taken, paid back duly, delays, critical accounts) |
| purpose                 | 4     | string (default) | Purpose of the credit (car, television, …)                         |
| credit_amount           | 5     | number (default) | Credit amount                                                       |
| savings_status          | 6     | string (default) | Status of savings account/bonds, in Deutsche Mark.                  |
| employment              | 7     | string (default) | Present employment, in number of years.                             |
| installment_commitment  | 8     | number (default) | Installment rate in percentage of disposable income                |
| personal_status         | 9     | string (default) | Personal status (married, single, …) and sex                        |
| other_parties           | 10    | string (default) | Other debtors / guarantors                                          |
| residence_since         | 11    | number (default) | Present residence since X years                                     |
| property_magnitude      | 12    | string (default) | Property (e.g. real estate)                                         |
| age                     | 13    | number (default) | Age in years                                                        |
| other_payment_plans     | 14    | string (default) | Other installment plans (banks, stores)                             |
| housing                 | 15    | string (default) | Housing (rent, own, …)                                              |
| existing_credits        | 16    | number (default) | Number of existing credits at this bank                              |
| job                     | 17    | string (default) | Job                                                                  |
| num_dependents          | 18    | number (default) | Number of people being liable to provide maintenance for            |
| own_telephone           | 19    | string (default) | Telephone (yes, no)                                                 |
| foreign_worker          | 20    | string (default) | Foreign worker (yes, no)                                            |
| accepted                | 21    | string (default) | Class                                                                |



# Results

#### Manually Tuned Models

| Model         | Test Score | Train Score |
|---------------|------------|-------------|
| RF_manually   | 0.932      | 0.937       |
| XGB_manually  | 0.924      | 0.929       |
| SVC_manually  | 0.520      | 0.522       |

#### Grid Search Tuned Models

| Model              | Score |
|--------------------|-------|
| RF_gridsearch      | 0.933 |
| XGB_gridsearch     | 0.931 |
| SVC_gridsearch     | 0.522 |


Best model chosen: Random Forest Classifier with dollowing parameters:  [n_estimators = 10, max_depth = 5, criterion = 'gini', class_weight = 'balanced', random_state = 42]


# Licence:
MIT 
