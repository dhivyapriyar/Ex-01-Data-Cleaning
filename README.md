# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
import pandas as pd

df=pd.read_csv("/content/Loan_data.csv")

print(df)

df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])

df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])

df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])

df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())

df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())

df.head()

df.info()

df.isnull().sum()

# OUPUT
![1](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/7dcdfc38-1369-4ff1-9c9d-e930573fcf4d)
![2](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/5cb050c7-da6a-4a19-9d97-1f06e73a7962)
![3](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/4553f0b6-ad5f-4392-8b3a-a722bf1cea11)
![4](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/e7361b8a-7aad-43dd-972f-e422e129c4d4)
![5](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/47984aea-9678-4c6c-8e13-99e160476d0b)
![6](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/d6ff1ff1-4538-416d-b0e0-c117593825f6)
![7](https://github.com/dhivyapriyar/Ex-01-Data-Cleaning/assets/119477552/8fd07b17-6fb7-417e-b504-b43c70ab83fb)

# RESULT
Thus, the given data is read, cleansed and the cleansed data is saved into the file.
