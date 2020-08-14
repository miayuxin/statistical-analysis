# statistical-analysis

## Goal
Learn to perform statistical analysis computationally, rather than mathematically, with programs written in Python. 
Work on the projects to investigate a series of statistical questions and interpret the results. 

## Dataset
This repository is based on the book: [Think Stats (Second edition)](https://www.oreilly.com/library/view/think-stats-2nd/9781491907344/) by Allen B. Downey.
The dataset is the National Survey of Family Growth (NSFG) from US Centers for Disease Control and Prevention (CDC).

## Content
I used Python to conduct the probability and statistics analysis, from collecting data and generating statistics to identifying patterns and testing hypotheses.

1. Exploratory Data Analysis
- Cross-validated the respondent and pregnancy files by comparing pregnum for each respondent with the number of records in the pregnancy file.
- Used nsfg.MakePregMap to make a dictionary that maps from each caseid to a list of indices into the pregnancy DataFrame.

2. Distributions
- Investigated whether first babies are lighter or heavier than others.
- Computed Cohen’s d to quantify the difference between the groups, and analyzed how does it compare to the difference in pregnancy length?

3. Probability Mass Functions
- Wrote functions called PmfMean and PmfVar that take a Pmf object and compute the mean and variance. 
To test these methods, checked that they are consistent with the methods Mean and Var provided by Pmf.
- Addressed the questions of “Are first babies more likely to be late?” 
- Computed the difference in means between groups of babies, by selecting respondents who have at least two babies and computed pairwise differences; determined whether this formulation of the question yield a different result.

4. Cumulative Distribution Functions
- Used the NSFG data (all live births) to compute the distribution of birth weights and use it to find the percentile rank.
- Generated 1,000 numbers from random.random and plotted their PMF and CDF, to determine whether the distribution is uniform.

5. Probability Density Functions
- Computed the median, mean, skewness and Pearson’s skewness of the household incomes sample from the Bureau of Labor Statistics and the Census Bureau. 
- Addressed the questions of "What fraction of households reports a taxable income below the mean?", and "How do the results depend on the assumed upper bound?"

6. Linear Least Squares
- Used the data from the BRFSS to compute the linear least squares fit for log(weight) versus height.
- Used resampling, with and without weights, to estimate the mean height of respondents in the BRFSS, the standard error of the mean, and a 90% confidence interval; 
identified that how much does correct weighting affect the estimates. 

