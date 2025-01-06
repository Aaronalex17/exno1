# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
###### import pandas as pd 
###### df=pd.read_csv("/content/sampleIDS/.csv")
###### df





###### df.head()

###### df.tail(5)



###### df.isnull()


df.notnull()


df.dropna(axis=0)


df.dropna(axis=1)


###### df.fillna(0)


### IQR:
import pandas as pd 
##### import seaborn as sns
##### ir=pd.read_csv('/content/iris.csv')
##### ir


ir.describe()


sns.boxplot(x="sepal_width',data=ir)



c1=ir.sepal_width.quantile(0.25)
c3=ir.sepal_width.quantile(0.75)
iq=c3-c1
print(c3)
#### =3.3
rid=ir[((ir.sepal_width<(c1-1.5*iqr))&(ir.sepal_width>(c3+1.5*iqr)))]
rid["sepal_width]
dtype:float64
###### delid =ir[~()ir.sepal_width<(c1-1.5*iqr))&(ir.sepal_width>(c3+1.5*iqr)]

##### delid

sns.boxplot(x="sepal_width",data=delid)

### z score


impot matplotlib.pyplot as plt
##### import pandas as pd
###### import numpy as np
import scipy .stats as stats
###### dataset=pd.read_csv("/content/heights.csv")
dataset



df=pf.read _csv("heights.csv")
###### q1=df["heights"].quantile(0.25)
###### q2=df["heights"].quantile(0.5)
###### q3=df["heights"].quantile(0.75)
iqr=q3-q1
###### =0.9249999999998

low=q1-1.5*iqr
###### low
##### =3.8625000000000003
high=q2+1.5*iqr
###### high
##### =7.5625

df11=df[((df["heights"]>=low)&(df["heights"]<=high))]
###### df11


z=np.abs(stats.zscore(df["heights"]0))
###### z


df11=df[z<3]
###### df11



```
# Result:
        thus the data cleaning process and detecting and removal of outliers are executed sucessfully

