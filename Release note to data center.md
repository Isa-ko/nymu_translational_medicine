# NYMU BMI translation of medicine stroke project (analysis center) <br>
Editor: Isa ko <br>
The aim of this document is to introduce the files restored to data center :
## Model_data.csv
This is the model training dataset, and the size of data is **(5720,11)**.
Exclusion criteria and work flow :

![image](https://user-images.githubusercontent.com/69064353/115986561-53fa3d80-a5e3-11eb-9c69-97091af2d10b.png)

feature	|content	|Imputation of missing value
-------|-----------|-----------------
yr|	numeric|	No missing value
pid	|string|	No missing value
psick11|	0: No 1: yes|	No missing value
gender	|1: male 2: female	|No missing value
age	|numeric	|mean
g_ssr	|numeric|	mean
g_bmi	|numeric|	mean
mdrug07|	0: No 1: yes|	mod
psick10|	0: No 1: yes|	mod
drinkornot_98	|(1)不喝或每週少於1次(選擇"不喝或每週少於1次"者跳答下一大題) (2)以前喝，現已戒酒  (3)每週1-2次  (4)每週3-4次  (5)每天喝	
drinkornot_group|	0: No 1: yes	|mod

## Logistic_F2.pkl

This is logistic regression model which was built by analysis center


## mj_data_final_edit.ipynb、MJ data cutoff.ipynb
These two are Programming files. The former is including preprocessed data (clean、selection、imputation) and also build model(five algorithm); the latter is to find stroke probability equation and cutoffs by logistic regression
