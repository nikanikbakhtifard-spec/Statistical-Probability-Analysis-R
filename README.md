# Statistical Probability Analysis in R

**Conditional Probability, Bayes' Theorem, Probability Distributions and Sampling**

## Project Overview

This project analyzes card transactions using R to explore core statistical probability concepts. It examines how payment-channel characteristics relate to automated fraud alerts, evaluates fraud-detection performance using Bayes' theorem, models event counts and waiting times, and illustrates sampling distributions through simulation.

The analysis was completed in an R Markdown notebook as part of a university statistical probability exercise.

## Dataset

`L17_transactions.csv` contains **12,000 transactions** across **60 days** (200 transactions per day). The eight variables describe transaction identifiers, day, time of payment, weekend status, payment channel, transaction amount, audited fraud status and automated alert status.

| Dataset metric | Value |
|---|---:|
| Transactions | 12,000 |
| Recorded fraud cases | 189 |
| Fraud prevalence | 1.575% |
| Alerts raised | 545 |
| Overall alert rate | 4.54% |
| Missing values | 0 |

## Analysis

### 1. Conditional Probability and Independence

- Estimated overall alert probability and alert probabilities for web and POS payments.
- Compared observed joint probabilities with products of marginal probabilities to examine empirical departures from independence.

### 2. Bayes' Theorem and Fraud Detection

- Built a confusion matrix using audited fraud status and detector alerts.
- Calculated sensitivity, specificity and positive predictive value (PPV).
- Compared empirical diagnostic measures with separately specified certified detector rates using Bayes' theorem.

### 3. Probability Distributions

- Compared Binomial and Poisson models for fraud counts among 200 transactions.
- Examined daily alert-count means and variances.
- Studied within-day waiting times between alerts using an exponential model.

### 4. Sampling Distributions

- Summarized transaction amounts and their skewness.
- Simulated 2,000 sample means for each sample size (**n = 5, 30 and 100**) to illustrate the Central Limit Theorem and standard-error behavior.
- Checked normal-approximation conditions for the sample fraud proportion at **n = 200 and 1,000**.

## Selected Results

| Indicator | Observed result |
|---|---:|
| Fraud-detection sensitivity | 93.65% |
| Fraud-detection specificity | 96.88% |
| Positive predictive value (PPV) | 32.48% |
| False alarms | 368 |
| Fraud cases without an alert | 12 |
| Mean daily alerts | 9.08 |
| Mean transaction amount | €48.53 |
| Median transaction amount | €29.39 |

**Main finding:** The detector identifies most fraudulent transactions, but only about one-third of its alerts correspond to actual fraud. This illustrates how a low underlying fraud prevalence affects the interpretation of positive alerts, even when sensitivity and specificity are high.

The observed data describe this transaction portfolio; they do not establish causal relationships or guarantee detector performance in other populations.

## Repository Files

- `L17_Exercise_Completed.Rmd` — Completed R Markdown analysis, including code, calculations and visualizations.
- `L17_Exercise_Completed.html` — Rendered report for viewing in a browser.
- `L17_transactions.csv` — Input dataset (include only if distribution is permitted).

## Reproduce the Analysis

1. Install **R** and **RStudio**.
2. Install the required packages in R: `install.packages(c("rmarkdown", "knitr"))`.
3. Place `L17_Exercise_Completed.Rmd` and `L17_transactions.csv` in the **same folder**.
4. Open the `.Rmd` file in RStudio and select **Knit** to generate the HTML report.

The notebook uses base R for its numerical calculations and sets a random seed for the sampling simulation.

## Tools

R · R Markdown · RStudio · `rmarkdown` · `knitr`

## Data Use

The transaction dataset was supplied for an academic exercise. Redistribution or public sharing should be confirmed with the data provider before making this repository public.
