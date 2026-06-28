# Task 1: Business Problem Statement

## Business Problem

The company has introduced a new onboarding and activation campaign for newly signed-up users. Users have been randomly assigned to either the Control group (existing onboarding experience) or the Treatment group (new campaign experience).

The key business decision is to determine whether the new onboarding experience should be rolled out to all users based on its impact on user conversion and early engagement.

### 1. Decision to be Made

The leadership team needs to decide whether the new onboarding campaign (Treatment group) should replace the existing onboarding experience for all future users.

### 2. Stakeholders Impacted

The decision will impact multiple stakeholders, including:

- Product Management Team
- Growth and Marketing Team
- User Experience (UX) Team
- Business Leadership
- Existing and New Users

### 3. Metrics That Should Improve

The primary success metrics are:

- User conversion rate
- Trial start rate
- Onboarding completion rate
- Activation rate
- Early user engagement

Secondary metrics may include:

- Retention rate
- Paid subscription conversion rate

### 4. Risks That Must Be Monitored

While evaluating the experiment, the following risks should be monitored:

- Decrease in onboarding completion rates
- Reduced user engagement for specific segments
- Negative impact on mobile or desktop users
- Lower conversion rates in certain regions or traffic sources
- Increased drop-off during the onboarding process

These metrics act as guardrail metrics to ensure that improvements in one area do not negatively impact other important business outcomes.

### 5. Evidence Required Before Recommendation

Before recommending a full rollout, the following evidence is required:

- Comparison of key metrics between Control and Treatment groups.
- Statistical significance testing to confirm that observed differences are not due to random variation.
- Analysis of guardrail metrics to ensure no adverse effects.
- Segment-level analysis across device type, region, traffic source, and plan type.
- Overall business impact assessment.

The treatment should only be launched if it demonstrates statistically significant improvements in conversion and engagement without negatively affecting guardrail metrics.


# Task 2: North Star Metric

## Selected North Star Metric

### North Star Metric: Onboarding Completion Rate

The North Star Metric selected for this experiment is **Onboarding Completion Rate**, which measures the percentage of users who successfully complete the onboarding process after signing up.

---

## Why This Is the Main Success Metric

The primary objective of the new onboarding campaign is to improve user activation and early engagement. Users who complete onboarding are more likely to understand the product, engage with key features, start trials, and eventually become paying customers.

Therefore, onboarding completion rate directly reflects the effectiveness of the new onboarding experience and serves as the most important measure of experiment success.

---

## Why Other Metrics Are Supporting Metrics

Other metrics such as:

- Landing page visit rate
- Trial start rate
- Conversion rate
- Retention rate
- Paid subscription rate

are considered supporting metrics because they measure specific stages of the user journey.

While these metrics provide additional insights, they do not directly capture whether users successfully complete the onboarding experience.

Hence, they support the North Star Metric rather than replacing it.

---

## How This Metric Connects to Business Growth

Improving onboarding completion can positively impact business growth in several ways:

- More users become activated.
- Activated users are more likely to start free trials.
- Trial users are more likely to convert into paying subscribers.
- Better onboarding increases user retention and engagement.
- Higher retention leads to increased revenue and customer lifetime value.

As a result, improvements in onboarding completion directly contribute to long-term business growth.

---

## Risks of Optimizing This Metric Blindly

Optimizing onboarding completion without monitoring guardrail metrics may create unintended consequences.

Potential risks include:

- Users may complete onboarding without genuinely understanding the product.
- The onboarding flow may become too aggressive or misleading.
- User satisfaction could decrease.
- Conversion quality may decline despite higher completion rates.
- Certain user segments may experience a worse overall experience.

Therefore, onboarding completion should always be evaluated together with engagement, retention, and conversion metrics.


# Task 4: Clean and Prepare Experiment Data

### Missing Values Check

The dataset was checked for missing values using filters.

Findings:
- `device_type` contained 18 missing values.
- `traffic_source` contained 24 missing values.
- `days_to_convert` contained 1336 missing values.
- `engagement_score` contained 14 missing values.

Actions Taken:
- Missing `device_type` values were replaced with "Unknown".
- Missing `traffic_source` values were replaced with "Unknown".
- Missing values in `days_to_convert` were retained because users who did not convert do not have a valid conversion duration.
- Missing `engagement_score` values were retained as blank due to insufficient information to accurately impute the scores.

### Group Count Check

The distribution of users across experiment groups was checked.

Findings:
 - Control Group: 693 users
 - Treatment Group: 715 users

Conclusion:
- The experiment groups are reasonably balanced, with only a small difference in user count. Therefore, the dataset is suitable for A/B   testing and comparison between groups.



### Duplicate User ID Check

The `user_id` column was checked for duplicate values using Excel filters and conditional formatting.

Findings:
- 8 duplicate user IDs were identified in the dataset.

Action Taken:
- Duplicate records were reviewed and found to be exact duplicates. These duplicate records were removed before analysis to avoid bias in experiment results.


### Invalid Binary Values Check

- The binary columns (`visited_landing_page`, `started_trial`, `completed_onboarding`, and `converted_to_paid`) were checked to ensure that they contained only valid binary values (0 or 1).

Findings:
- No invalid binary values were found. All records contained only valid values (0 and 1).

Action Taken:
- No action was required as the data was already valid.



### Outliers in Revenue Check

- The `revenue_30d` column was reviewed by sorting the values from highest to lowest and applying conditional formatting.

Findings:
- Several unusually high revenue values were identified as potential outliers. Examples include revenue values above 1000.

Action Taken:
- These records were retained in the dataset because they may represent genuine high-value customers and are important for business analysis. The outliers were flagged for monitoring during analysis.



### Segment Distribution Across Groups

 - The distribution of key customer segments such as device type, region, and plan type was reviewed across the Control and Treatment groups using Excel filters.

 Findings:
 - Customer segments were found to be reasonably distributed across both experiment groups, with no major imbalance observed.

Action Taken:
 - No corrective action was required as the segment distribution was balanced and suitable for experiment analysis.




