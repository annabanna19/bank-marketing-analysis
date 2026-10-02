# Bank Marketing Campaign Analysis

**Question:** Which customers and contact approaches are most associated with signing up to a bank's term-deposit campaign?

## Data
UCI Machine Learning Repository, Bank Marketing dataset (Moro, Cortez & Rita, 2014). 45,211 phone-campaign contacts from a Portuguese bank, 17 variables. Overall sign-up rate: 11.7%.

## Approach
- Cleaned the data in pandas: identified missing values coded as "unknown", relabelled previous-outcome unknowns as "not contacted" (36,954 of 36,959 were never previously contacted), and excluded call duration because it is only known after the call.
- Compared sign-up rates by age, occupation, previous campaign outcome and contact channel, with charts in matplotlib.
- Fitted a logit model (statsmodels) and reported average marginal effects to test whether patterns held after controlling for other factors.

## Key findings
- Customers who responded to a previous campaign signed up at 64.7%, and this was the strongest predictor in the model (+43.8 percentage points).
- Over-65s and 18 to 25 year olds converted well above average, and the age effect persisted after controlling for occupation.
- Previous non-responders' apparent advantage over never-contacted customers was not significant once other factors were controlled for.
- The 29% of contacts with no recorded channel converted at 4.1%, which suggests a data-quality issue worth investigating.

## Limitations
Results are associations from historical data, not causal effects, and come from one bank's campaigns.

## Tools
Python (pandas, matplotlib, statsmodels), Google Colab.
