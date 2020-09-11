Credit Risk Modelling:
Not just a classification problem! Have a look at domain knowledge and reqirements and get more out of your data, Calculating probablility of default, creating scorecards for individuals, calculating Loss given default, Exposure at default & expected loss for individuals for loan approval via IRB Advanced approach.

Refer Credit_Risk_Model.pptx for details about problem statement we are trying to solve.

For Dataset mail me at akashbm08@gmail.com

Below is decription about flow and files required for each codes to run and files generated after each.

Raw Data: 
    1. LCDataDictionary.xlsx (Reference for fields/columns)
    2. loan_data_2007_2014.csv


Part 1: Preprocessing:
(Eg WoEIV file contains ref example for WOE/IV)
(Files required to run loan_data_2007_2014.csv)

Code:
    1. Preparation.ipynb
    2. Preparation_test.ipynb (for same preprocessing for test data)

O/p: Data Stored in:
    1. loan_data_inputs_test.csv
    2. loan_data_inputs_train.csv
    3. loan_data_targets_test.csv
    4. loan_data_targets_train.csv

Part 2: PD modelling and Validation: 
(Files required to run: All O/p files from part 1)
Code:

1. PD_model.ipynb


O/p: Model stored in:
    1. pd_model.sav
    2. df_scorecard.csv
    3. inputs _train_with_ref_cat.csv


Part 3: LGD, EAD, EL:

(Files required to run: 
    1. loan_data_2007_2014_preprocessed.csv (Preprocessed file from part 1 as required)
    2. O/p file pd_model.sav from part 2
    3. O/p files from part 1 with prefix ‘loan_data_inputs’)

Code:
    1. LGD_EAD_EL.ipynb

O/p: Model/Files stored in:
    1. lgd_model_stage_1.sav (Stage 1: logistic regression)
    2. lgd_model_stage_2.sav (Stage 2: linear regression)
    3. loan_data_defaults.csv (Data just with default customer entries)

For more info about data source: https://www.lendingclub.com/info/statistics.action
