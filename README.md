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
8. Prediction
9. LIME Interpretability of Predictions
10. Final Conclusion


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

Best model chosen: Random Forest Classifier with dollowing parameters:  [n_estimators = 20, max_depth = 5,min_samples_split = 3, min_samples_leaf = 1, criterion = 'entropy', class_weight = 'balanced', random_state = 42]


# Prediction Data
| checking_status | duration | credit_history                       | purpose               | credit_amount | savings_status               | employment | installment_commitment | personal_status                      | other_parties | residence_since | property_magnitude        | age | other_payment_plans | housing | existing_credits             | job                           | num_dependents | own_telephone | foreign_worker |
|-----------------|----------|-------------------------------------|-----------------------|---------------|------------------------------|------------|------------------------|--------------------------------------|---------------|-----------------|---------------------------|-----|----------------------|---------|------------------------------|-------------------------------|---------------|---------------|----------------|
| 0_checking      | 24       | Delay_in_past                        | business              | 2745          | <100DM                       | <1yr       | 1                      | female_divorced/separated/married    | guarantor     | 2               | car_or_other_nonsavings    | 27  | none                 | for_free | 1                            | skilled_employee/official     | 2             | yes           | yes            |
| 0_checking      | 12       | Existing_credits_paid_till_now       | new_car               | 5500          | <100DM                       | 1_to_4yrs  | 4                      | male_single                          | co-applicant  | 4               | car_or_other_nonsavings    | 33  | none                 | own     | 1                            | skilled_employee/official     | 1             | yes           | yes            |
| 0_checking      | 18       | Existing_credits_paid_till_now       | radio/television      | 1500          | Unknown_or_no_savings_acct   | <1yr       | 4                      | male_married/widowed                 | guarantor     | 2               | unknown/no_property        | 25  | stores               | rent    | 1                            | unskilled_resident            | 1             | yes           | yes            |

Predictions: [0 1 0]

Prediction probabilities:
 [[0.84816025 0.15183975]
 [0.07250454 0.92749546]
 [0.96737706 0.03262294]]

# LIME Interpretability
![1](https://github.com/user-attachments/assets/c0fd19ea-5279-465b-b191-b7fdf9e41eac)

![2](https://github.com/user-attachments/assets/f015f632-adfd-48de-b880-52e1ccaf0287)

![3](https://github.com/user-attachments/assets/38799ea2-51a8-4265-913a-586c74b06436)

 
# Licence:
MIT 
