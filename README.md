# Prosper Loan Dataset Exploration

This project constitutes a part of my Udacity Data Analyst Nanodegree program. The project was in two parts and involved carrying out; Exploratory and Explanatory data visualization. 

After carrying out some data wrangling steps, for exploratory data visualization, I made use of Python visualization libraries such as seaborn and matplotlib to explore and carry out plots of single variables (univariate exploration), and multiple variables (bivariate and multivariate exploration).

For explanatory data visualization, I was able to produce a short presentation illustrating some interesting properties/trends discovered in the data. 

## Dataset

The original dataset contains 113,937 entries with 81 features. The majority of the variables under the respective features were numeric in nature with an exception of some variables with string input e.g (ListingKey, ListingCreationDate, CreditGrade, LoanStatus, ClosedDate, ProsperRating (Alpha), BorrowerState, Occupation, EmploymentStatus, GroupKey, DateCreditPulled, FirstRecordedCreditLine, IncomeRange, LoanKey,  LoanOriginationDate, LoanOriginationQuarter, MemberKey) or boolean values such as the features ('IsBorrowerHomeowner','CurrentlyInGroup', and 'IncomeVerifiable'). Some features also contain missing values.


## Summary of Findings
During expoloration, the overall goal is to address if a borrower's income can affect the status of a loan’s outcome. For Univariate exploration, the variables of interest chosen were the 'ProsperScore', 'IncomeRange', 'DebtToIncomeRatio', 'IncomeVerifiable', 'StatedMonthlyIncome', 'CreditScoreRangeLower', and 'CreditScoreRangeUpper'. The distribution of the DebtToIncomeRatio, StatedMonthlyIncome, CreditScoreRangeLower, and CreditScoreRangeUpper displayed a left-skewed or negative-skewed distribution, indicating that the preferred measure of central tendency is mean. The distribution is also unimodal that is having one peak(or mode). To my knowledge, no unusual points were identified. 

Moving further, for bivariate exploration, I observed a negative correlation (-0.115) exist between the DebtToIncomeRatio and the StatedMonthlyIncome, as well as between the DebtToIncomeRatio and ProsperScore (-0.163) indicating that as one variable increases, the other variable decreases in turn. On the other hand, there is almost no correlation (0.097) between the StatedMonthlyIncome and ProsperScore features.

Finally, with multivariate exploration, I was quite surprised that even with a high income range (>100,000USD), a borrower is still marked as high risk once they are not able to provide proof of documentation to back up their income. This could be associated with the fact that some unexpected life events could happen and in the case of this happening, if there is no guarantee for the borrower to pay back a loan, it puts the lender is at risk of losing their money. In summary this indicates that the IncomeVerifiable feature plays a major role in determining if a loan will be granted or not.

## Key Insights for Presentation
My focus for the presentation were similar to the findings in the notebook. However the presentation provided a more compact summary. The key features visualized under the univariate exploration were for the 'ProsperScore', and 'IncomeVerifiable'.

For Bivariate exploration, the visualization plot included the pairwise correlations between the numerical features of interest;'ProsperScore', 'DebtToIncomeRatio', and 'StatedMonthlyIncome' using a heatmap and plotting a matrix of 500 sample loans in the data. The heatmap showed a negative correlation between the DebtToIncomeRatio and the StatedMonthlyIncome, and almost no correlation (0.097) between the StatedMonthlyIncome and ProsperScore. The matrix plot displayed the distribution of the DebtToIncomeRatio and StatedMonthlyIncome as a left-skewed and a unimodal distribution, while the ProsperScore in contrast displayed a right-skewed distribution. 

Finally, for Multivariate Exploration, a heat map was plotted showing the Median ProsperScore by the IncomeRange and IncomeVerifiable. In summary, the plot confirmed that the IncomeVerifiable feature (which indicates the borrower's ability to provide documentation in backing up their income) plays a major role in determining if a loan will be granted or not.
