Link to gDrive with https://drive.google.com/drive/folders/1t9HZFnQ_-QgNF59-pHUlWlYFcV-C2Ffo?usp=sharing

# Quantitative Trading and Analysis with Python: Course project (group)
**Due: Fri Mar 31, 2023 11:59pm**

**The ultimate goal:** improve the performance of a specified portfolio using option-implied signals.

**Description:** 

1. You are given 50 stocks from the S&P500 universe. Use a value-weighted (market-cap-weighted) portfolio of these stocks from 01/2000 until 12/2021 as your starting point, that is, as your benchmark portfolio [BNCH]. Note: you can use all stocks in your universe (not just 50), but be careful not to overstretch the capacity of your computers!
2. Using the in-sample period from 01/2000 until 12/2015, create a quant strategy [QS] that improves upon the BNCH in terms of performance under specific constraints. 
3. [additional explanation added] Using the model that you selected in the in-sample period (e.g., LASSO, or RIDGE, etc), create your QS, analyze and report performance for the out-of-sample period from 1/2016 until 12/2021; you still can use a rolling window approach, re-estimate model parameters, but you do not change your model in this period. 
4. *Performance metrics and constraints:* 
    * Performance can be measured in terms of Sharpe Ration, Variance, Excess Return w.r.t. BNCH. For example, you achieve positive and statistically significant excess return given the same or lower variance, or lower variance conditional on the same or higher excess return.
    * *Constraints imposed:*
        * Factor exposure deviation from BNCH max 0.05 [for each considered factor]. For example, if the benchmark has 20% Value Factor exposure (beta), let the target portfolio deviate at most   5% with respect to the 20% exposure (i.e., to be between 15% and 25%).
        * Weight deviation for each asset max 10% of the BNCH weight, i.e., if the weight of an asset is 1%, the weight of that asset in your portfolio can be between 0.9% and 1.1%. 
    * Drawdown relative to BNCH max 1% per month [that is, QS shall not lose more than 1% of its value per month compared to the BNCH].

**Data:**

1. The list of stocks in terms of PERMNO -- the same list as for Homework 2/ available on Dropbox
2. The data on factors is available at the Ken French web-site [use the 4-factor model]
3. Selected ready-to-use option-implied data available on https://osf.io/z2486

specifically, you can use:  
    - Generalized lower bounds https://osf.io/7xcqw links to an external site from https://dx.doi.org/10.2139/ssrn.3565130  
    - Risk-neutral skewness https://osf.io/btvdh/ from http://dx.doi.org/10.2139/ssrn.1301648  
4. Any other features you might find useful (technical analysis, sentiment, price patterns, etc.)
5. WRDS data on stock returns [CRSP], options [OptionMetrics], fundamentals [COMPUSTAT]


**Submission:**

*Please submit a zip file containing:* 

1. A report in PDF documenting the final results. 
2. Jupyter Notebook with the code generating your results/ do not submit any data to Canvas.
3. If you use any data loaded from files in the Jupyter Notebook, please put these data to an online data storage, and specify the link to how we can access it. 