# Hypothesis Test Notes

## Metric Tested
Paid Conversion Rate (converted_to_paid)

## Null Hypothesis (H0)
There is no significant difference in paid conversion rate between the Control and Treatment groups.

## Alternative Hypothesis (H1)
The Treatment group has a significantly higher paid conversion rate than the Control group.

## Test Type
One-tailed independent two-sample t-test (assuming unequal variances).

## Significance Level
Alpha = 0.05

## Reason for Choosing this Metric
Paid conversion rate is the primary business metric because it directly measures the effectiveness of the experiment in converting users into paying customers.

## Test Inputs
- Control group size: 693 users
- Treatment group size: 715 users
- Control mean conversion rate: 3.17%
- Treatment mean conversion rate: 6.99%

## Test Output
- t-statistic = -3.2801
- p-value (one-tail) = 0.00053

## Decision Rule
Reject the null hypothesis if p-value < 0.05.

## Interpretation Logic
Since the p-value (0.00053) is less than the significance level (0.05), we reject the null hypothesis.

## Business Interpretation
The Treatment group achieved a significantly higher paid conversion rate than the Control group. This indicates that the new treatment had a positive impact on user conversion and should be considered for implementation.
