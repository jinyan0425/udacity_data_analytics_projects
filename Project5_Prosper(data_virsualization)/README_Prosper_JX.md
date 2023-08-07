# What Affects Lender's Contribution to Peer-to-peer Lending? -- An Exploration on the Antecedants.
## by Jinyan Xiang


## Dataset

The dataset is retrieved from Prosper.com - a leading p2p lending platform in the US. Borrowers on the platform can create loan listings seeking p2p lending, and lenders can lend money to borrowers and gain interest in return. Data can be downloaded from https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv. A detailed description of each variable in this dataset can be found at https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0. 

The original dataset contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. 

After data processing including excluding duplicated or/and not-fully-funded loans and outliers, the dataset contains 110,579 unique fully-funded Prosper loan listings created and funded between November 2005 and March 2014 in 51 US states and Washington DC. In addition, I created three new variables -- LoanDuration -- how long the loan was listed between being listed and being fully funded, ListingYear -- which year the listing was listed, and AverageLending -- how much investors invested in a listing on average. Note that AverageLending is the focal outcome variable in this exploration because it is a proxy of the lender's contribution to the p2p lending and more broadly, engagement in the sharing economy, which is a  crucial metric that both sharing economy platforms and policymakers are interested in.

## Key Research Questions

I focused on two major questions in this exploration. 

First, what are the antecedents of lenders' average lending amount? I explore this question from factors in three facets - borrowers', lenders', and loans'. Specifically, I aimed to examine how 1) borrowers' prosper score -- an integrated metric of the borrower's credibility and stated monthly income -- an indicator of the borrower's payoff ability, 2) lenders' yield -- an indicator of ROI of the lending, as well as 3) the loans' term -- a factor that affects ROI rate affects average lending amount. In addition, I also explored the interactions between these focal predictors.

Second, what are the regional patterns and historic trends of p2p lending  more broadly, the sharing economy, which was reflected by the listing distributions across states and years?

## Summary of Findings

With both various types of visual explorations (e.g., univariate, bivariate, and multivariate) and multiple auxiliary statistical analyses (e.g., Pearson correlation, ANOVA, robust linear regression), I found:
1) borrower's prosper score, which is an integrated metric of the borrower's credibility and reliability, has a nuanced relationship with the average lending amount in that there is a positive relationship when the prosper score is relatively low (1-4) and almost no relationship when it is in the middle (5-7) and regain a generally positive relationship when it is high (8-11) - more complicated than the prediction.
2) Borrowers' stated monthly income had a positive effect on the average lending amount.
3) Lenders' yield has a surprisingly negative effect on the average lending amount.
4) Loans' term was positively related to the average lending amount (i.e., the longer term (e.g., 60 months vs. 12 months), the more average lending amount).
5) Loans' duration was also negatively related to the average lending amount (i.e., the longer duration, the less average lending amount).
6) Loan's listing year had a U-shaped relationship with the average lending amount in that it decreased from 2005 to 2010 and dramatically increased since 2010.
7) There was a significant interaction between the prosper score and stated monthly income, both suggesting borrowers' credibility; specifically, the borrower's stated monthly income had a stronger positive influence on the average lending amount for borrowers with a high (vs. med) prosper score.
8) There was a significant interaction between borrowers' prosper score and lenders' yield, which reflects a tradeoff between risk and return of the investment for lenders; interestingly, lenders' yield has significant negative effects on average lending amount when borrowers have low and med prosper score; however, it has no effect on average lending amount when borrowers have high prosper score.
9) There was a significant interaction between loans' term and lenders' yield, both suggesting lenders' ROI rate; specifically, lenders' yield had a negative effect on the average lending amount when the loans' term is 60 months; however, it has no effects on the average lending amount when loans' term is 12 or 36 months.

10) P2p lending is more popular in states with better economies (in terms of GDP, CA > TX > NY > FL > IL).
11) P2p lending became more popular in recent years, especially after 2009. The sudden drop in 2009 was possibly due to the Financial crisis of 2007–2008.


## Key Insights for Presentation

For the presentation, I focused on just how borrowers' prosper scores and stated monthly income, lender's yield, and loan term as well as their interactions affect lender's average lending amount.

I start by introducing the investigation background (i.e., empirical context) and goals, followed by a brief description of the dataset.

Then, I elaborate on the rationales for selecting the outcome variables (i.e., average lending amount) and predictors, as well as how the outcome variable was created.

Next, I show the distribution of the outcome variable and focal predictors with histograms (for continuous variables - average lending amount, stated monthly income, and lender's yield) and bar charts (for discrete and categorical variables - prosper score and loan's term). 

Afterward, I use a correlation matrix and scatter plots (for quantitative variables), and bar chart (for categorical variables) to show the bivariate relationships between each predictor and the outcome variable.

Finally, I use regression plots to show the interactions between the borrower's prosper score and stated monthly income, between the borrower's prosper score and the lender's yield as well as between the lender's yield and loan term.
