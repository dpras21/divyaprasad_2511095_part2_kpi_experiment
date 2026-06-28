# KPI Experiment Analysis

## 1. Business Context

The company conducted an A/B experiment to evaluate whether a new product experience (Treatment group) performs better than the existing experience (Control group). The primary objective was to improve paid user conversions while ensuring that user experience and business health metrics were not negatively impacted.

---

## 2. Dataset Description

The dataset contains user-level experimental data with the following information:

- User ID
- Experiment Group (Control/Treatment)
- Landing Page Visit
- Trial Start Status
- Onboarding Completion Status
- Paid Conversion Status
- Revenue generated in 30 days
- Refund Requests
- Support Tickets
- Engagement Score
- Days to Convert
- Region
- Device Type
- Traffic Source

Total Users:
- Control Group: 693 users
- Treatment Group: 715 users

---

## 3. North Star Metric Selected

**North Star Metric:** Paid Conversion Rate

This metric was selected because increasing the number of users who become paying customers is the primary business objective.

---

## 4. KPI Tree Summary

The Paid Conversion Rate is influenced by several supporting KPIs:

```
Landing Page Visit
↓
Trial Start
↓
Onboarding Completion
↓
User Engagement
↓
Paid Conversion
↓
Revenue
```

Improvements in upstream metrics are expected to positively impact conversions.

---

## 5. Experiment Analysis Approach

The following steps were performed:

1. Data quality checks.
2. Missing value identification and treatment.
3. Calculation of business KPIs for Control and Treatment groups.
4. Segment-level analysis by Region, Device Type, and Traffic Source.
5. Hypothesis testing using a two-sample t-test.
6. Evaluation of guardrail metrics.
7. Final business recommendation.

---

## 6. Hypothesis Test Summary

A two-sample t-test assuming unequal variances was performed on the Paid Conversion metric.

### Hypotheses

- **Null Hypothesis (H0):** Treatment does not improve paid conversion compared to Control.
- **Alternative Hypothesis (H1):** Treatment improves paid conversion.

### Test Details

- Significance Level (α): 0.05
- P-value: 0.00053

Since the p-value is less than 0.05, the null hypothesis was rejected.

**Conclusion:** The Treatment group significantly improved paid conversion.

---

## 7. Guardrail Metrics Considered

The following guardrail metrics were evaluated:

- Refund Rate
- Support Ticket Rate
- Average Engagement Score
- Average Revenue per Converted User
- Average Days to Convert

Observations:

- Support Ticket Rate increased in Treatment.
- Revenue per Converted User decreased.
- Engagement Score improved.
- Refund Rate increased slightly.

---

## 8. Final Recommendation

### Recommendation: Continue Testing / Gradual Rollout

Although the Treatment group significantly improved paid conversion rates, increased support tickets and reduced revenue quality indicate potential risks.

A phased rollout with continued monitoring is recommended.

---

## 9. Assumptions and Limitations

- Missing values existed in several columns.
- Missing values in `device_type` and `traffic_source` were replaced with "Unknown".
- Missing values in `days_to_convert` and `engagement_score` were retained.
- The experiment duration may not capture long-term customer behavior.
- Some segments contained fewer observations.

---

## 10. Screenshots Included

The following screenshots are included in the `screenshots` folder:

- KPI Summary Table
- Segment Analysis Pivot Tables
- Hypothesis Test Output
- Data Quality Checks
























