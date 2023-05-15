# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE

import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore (1).csv")

df.info()

df.isnull().sum()

import matplotlib.pyplot as plt

import numpy as np

sns.distplot(df['Sales'])

plt.axvline(x=np.mean(df['Sales']), c='red', ls='--', label='mean')

plt.axvline(x=np.percentile(df['Sales'],25),c='green', ls='--', label = '25th percentile:Q1')

plt.axvline(x=np.percentile(df['Sales'],75),c='orange', ls='--',label = '75th percentile:Q3' )

plt.legend()

sns.boxplot(x=df['Segment'], y=df['Sales'])

sns.scatterplot(x=df['City'], y=df['Sales'])

sns.boxplot(x=df['Region'],y= df['Sales'])

# OUPUT

<img width="734" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/34f5708a-2d10-4e92-92a7-40b458919c86">
<img width="213" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/643ea486-c0b5-4b1d-8457-37675bd8e05f">
<img width="119" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/7951f610-f721-43f5-a1e8-627b43de066a">
<img width="365" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/8769100f-7659-4aca-9217-53b7e54b06df">
<img width="365" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/bf9f4aa8-2524-4bd1-b420-f0063deff6f2">
<img width="383" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/e3f77293-72c3-4a53-9e6f-b32ff4d25864">
<img width="359" alt="image" src="https://github.com/subikshamalaisamy/Ex-08-Data-Visualization-/assets/87276633/db4291b6-e2b7-4704-a55d-4790d7e05c15">

# RESULT

Thus the Data Visualization is performed successfully on the given dataset.
