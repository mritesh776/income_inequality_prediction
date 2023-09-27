- No of values in the dataframe that have a leading or trailing whitespaces or both:  3058016 
stripped ✅

- Target variable renamed from 'income_above_limit' to 'income_status'.✅

- balance the data after splitting.

- same number of missing values in 'old_residence_reg' and 'old_residence_state' which may suggest that these can be related.
- 'residence_1_year_ago' and 'migration_code_change_in_reg', 'migration_code_move_within_reg', 'migration_prev_sunbelt' have same number of unchanged address 86864
- all columns related to migration can be summed up into one for model.

- 'country_of_birth_own', 'country_of_birth_father', 'country_of_birth_mother' can give some different kind of insights about migration and income status.
- **how many of the individuals have father and mother of different  country origin.?**
- 'mig_year' has no missing values and 2 unique values 94 and 95 which seems odd.
- how  'stocks_status' is related with income status?
- vet_benifit column has values 0,1 and 2 hard to know what 1 and 2 mean if we assume 0 means not getting benifit
- under_18_family column provides the individuals who are under_18 has how many parents present. It got many missing values does missing value means that the individual is not under_18. this can make a feature **is_under_18.** `household_summary` could help
- 'household_stat', 'household_summary' related
- 'total_employed' family members employed
- among 'class' from self employed how many are below and how many are above.
- do same for 'education'
- gender wise above below
- age wise above below


'?' this need to be converted to null


**Important for model** : 'tax_status', 'gains', 'losses', 'stocks_status', 'wage_per_hour', 'working_week_per_year', **check multicollinearity here**('industry_code' or 'industry_code_main'), **check multicollinearity here**('occupation_code' or 'occupation_code_main'), 'total_employed', 'age', 'gender', 'education', 'employment_commitment'


Shape of dataframe: (209499, 43)

Number of columns: 43
['ID', 'age', 'gender', 'education', 'class', 'education_institute', 'marital_status', 'race', 'is_hispanic', 'employment_commitment', 'unemployment_reason', 'employment_stat', 'wage_per_hour', 'is_labor_union', 'working_week_per_year', 'industry_code', 'industry_code_main', 'occupation_code', 'occupation_code_main', 'total_employed', 'household_stat', 'household_summary', 'under_18_family', 'veterans_admin_questionnaire', 'vet_benefit', 'tax_status', 'gains', 'losses', 'stocks_status', 'citizenship', 'mig_year', 'country_of_birth_own', 'country_of_birth_father', 'country_of_birth_mother', 'migration_code_change_in_msa', 'migration_prev_sunbelt', 'migration_code_move_within_reg', 'migration_code_change_in_reg', 'residence_1_year_ago', 'old_residence_reg', 'old_residence_state', 'importance_of_record', 'income_above_limit']

Number of Numerical columns: 13
['age', 'employment_stat', 'wage_per_hour', 'working_week_per_year', 'industry_code', 'occupation_code', 'total_employed', 'vet_benefit', 'gains', 'losses', 'stocks_status', 'mig_year', 'importance_of_record']

Number of Categorical columns: 30
['ID', 'gender', 'education', 'class', 'education_institute', 'marital_status', 'race', 'is_hispanic', 'employment_commitment', 'unemployment_reason', 'is_labor_union', 'industry_code_main', 'occupation_code_main', 'household_stat', 'household_summary', 'under_18_family', 'veterans_admin_questionnaire', 'tax_status', 'citizenship', 'country_of_birth_own', 'country_of_birth_father', 'country_of_birth_mother', 'migration_code_change_in_msa', 'migration_prev_sunbelt', 'migration_code_move_within_reg', 'migration_code_change_in_reg', 'residence_1_year_ago', 'old_residence_reg', 'old_residence_state', 'income_above_limit']

No Datetime column in your dataframe