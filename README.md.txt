# README.md

# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and engagement. Users were randomly assigned to either a Control group (existing onboarding experience) or a Treatment group (new onboarding experience). The objective is to determine whether the new onboarding experience should be launched to all users.

## Dataset Description

The dataset contains user-level experiment data for both Control and Treatment groups, including onboarding activity, trial starts, paid conversions, engagement scores, refunds, support tickets, revenue, traffic source, region, device type, and plan type.

## North Star Metric

**Paid Conversion Rate**

Paid Conversion Rate was selected as the North Star metric because it directly reflects business growth and recurring subscription revenue. Other metrics such as landing page visits, trial starts, and onboarding completion are supporting metrics that contribute to improving paid conversion.

## KPI Tree Summary

The KPI Tree uses Paid Conversion Rate as the North Star metric.

Primary KPI Drivers:

* User Acquisition
* User Activation
* User Engagement

Guardrail Metrics:

* Refund Rate
* Support Ticket Rate
* Average Days to Convert

## Experiment Analysis Approach

The experiment dataset was validated by checking:

* Missing values
* Duplicate User IDs
* Group distribution
* Invalid binary values
* Revenue outliers
* Segment distribution across Region, Device Type, Traffic Source, and Plan Type

Summary metrics were calculated separately for Control and Treatment groups.

## Hypothesis Test Summary

Null Hypothesis (H0):
The new onboarding campaign does not improve the paid conversion rate.

Alternative Hypothesis (H1):
The new onboarding campaign improves the paid conversion rate.

A significance level of 5% was assumed for evaluating the experiment.

## Guardrail Metrics Considered

* Refund Rate
* Support Ticket Rate
* Average Engagement Score
* Average Days to Convert

These metrics ensure that improvements in conversion do not negatively impact customer experience or product quality.

## Final Recommendation

The Treatment group demonstrated stronger user engagement, higher landing page visits, and improved trial starts. However, the Support Ticket Rate increased significantly compared to the Control group.

Recommendation:

**Continue testing with a phased rollout while investigating the increase in support tickets before launching to all users.**

## Assumptions

* Users were randomly assigned.
* Tracking events were recorded correctly.
* Missing values were treated according to business rules.

## Limitations

* Limited experiment duration.
* External marketing factors were not considered.
* Customer lifetime value was not included.

## Screenshots Included

* summary_metrics.png
* hypothesis_test_output.png
* kpi_tree_preview.png
