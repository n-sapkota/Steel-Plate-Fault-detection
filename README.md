# Steel plate fault detection

## Data Source

 The full dataset can be found [here](https://archive.ics.uci.edu/ml/datasets/steel+plates+faults).

 The 7 types of faults present in the data sets are

1. Pastry

2. Z_Scratch

3. K_Scatch

4. Stains

5. Dirtiness

6. Bumps

7. Other_Faults

## EDA and Outlier Elimination

First, exploratory data analysis (EDA) was done to get insights into the dataset. For this, histograms, box plots, kernel density distributions, and Pearson's correlation coefficient between features are analyzed. The noise and outliers present in the datasets are removed using the DBSCAN clustering algorithm and the applicability of noise removal techniques such as z- score and quartile range (IQR method) is examined. The data does not follow a normal distribution, as evidenced by the histogram and Q-Q plots. So, we are able to use the Z-Score method for outlier detection. Similarly, when the IQR outlier removal method is used, all data associated with the class k_scratch are removed.

## Feature Selection

To select the most prominent feature from the data, we used filter methods for univariate feature selection. Firstly, we used the variance threshold method to remove the low variance features, and then ANOVA F-value was used to further reduce the features and select the most potential ones.

## Learning algorithm

KNN is used to train the model and gives a 79 % test accuracy with only 18 features and 23 neighborhoods used.

 ## Relevent Paper
1. M Buscema, S Terzi, W Tastle, A New Meta-Classifier,in NAFIPS 2010, Toronto (CANADA),26-28 July 2010, 978-1-4244-7858-6/10 Â©2010 IEEE
2. M Buscema, MetaNet: The Theory of Independent Judges, in Substance Use & Misuse, 33(2), 439-461,1998

