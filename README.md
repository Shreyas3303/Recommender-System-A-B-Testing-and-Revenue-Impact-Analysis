
# Recommendation System A/B Testing and Evaluation

This notebook performs A/B testing and evaluation of different recommendation systems: a Popularity-based Baseline, an Alternating Least Squares (ALS) model, and a SASRec (Self-Attentive Sequential Recommendation) model. The evaluation focuses on key metrics such as Hits@10, Revenue from Hits, and Basket Coverage, using paired Wilcoxon signed-rank tests for statistical significance.

Additionally, the project integrates simulated consumer metrics like Churn Rate and Customer Lifetime Value (CLTV) to provide a more holistic business perspective.

## A/B Test Results Summary

The following visualizations and summaries present the comparison of the recommender systems across various metrics.

### ALS vs Popularity-based Baseline

This comparison evaluates the performance of the Alternating Least Squares (ALS) model against a simple popularity-based baseline.

#### Hits@10

![Hits@10 - ALS vs Baseline](fig_1_ALS_vs_Baseline_Hits@10.png)

*Results showed that ALS performed significantly better than the Popularity-based Baseline in Hits@10.*

#### Revenue from Hits

![Revenue from Hits - ALS vs Baseline](fig_2_ALS_vs_Baseline_Revenue.png)

*ALS also generated significantly more revenue from hits compared to the Popularity-based Baseline.*

#### Basket Coverage

![Basket Coverage - ALS vs Baseline](fig_3_ALS_vs_Baseline_Coverage.png)

*ALS provided significantly better basket coverage than the Popularity-based Baseline.*

### SASRec vs Popularity-based Baseline

This section compares the SASRec model against the Popularity-based Baseline.

#### Hits@10

![Hits@10 - SASRec vs Baseline](fig_4_SASRec_vs_Baseline_Hits@10.png)

*In this comparison, the Popularity-based Baseline performed significantly better than SASRec in Hits@10.*

#### Revenue from Hits

![Revenue from Hits - SASRec vs Baseline](fig_5_SASRec_vs_Baseline_Revenue.png)

*The Popularity-based Baseline generated significantly more revenue from hits compared to SASRec.*

#### Basket Coverage

![Basket Coverage - SASRec vs Baseline](fig_6_SASRec_vs_Baseline_Coverage.png)

*The Popularity-based Baseline also provided significantly better basket coverage than SASRec.*

### ALS vs SASRec

Finally, this section directly compares the ALS model with the SASRec model.

#### Hits@10

![Hits@10 - ALS vs SASRec](fig_7_ALS_vs_SASRec_Hits@10.png)

*ALS performed significantly better than SASRec in Hits@10.*

#### Revenue from Hits

![Revenue from Hits - ALS vs SASRec](fig_8_ALS_vs_SASRec_Revenue.png)

*ALS generated significantly more revenue from hits compared to SASRec.*

#### Basket Coverage

![Basket Coverage - ALS vs SASRec](fig_9_ALS_vs_SASRec_Coverage.png)

*ALS provided significantly better basket coverage than SASRec.*


## Overall Consumer Behavior Metrics (Simulated)

These metrics provide a high-level view of customer behavior. In a real-world scenario, these would be directly calculated from granular transaction data. Here, they are simulated for demonstration purposes.

### Churn Metrics

-   **Overall Churn Rate:** {consumer_churn_metrics['overall_churn_rate']:.2%}
-   **Number of Churned Users (Simulated):** {consumer_churn_metrics['num_churned_users']}
-   *(Based on a simulated {consumer_churn_metrics['total_users_considered']} users)*

### Customer Lifetime Value (CLTV) Metrics

-   **Overall Average CLTV:** ${consumer_cltv_metrics['overall_average_cltv']:.2f}
-   **CLTV Standard Deviation:** ${consumer_cltv_metrics['cltv_std_dev']:.2f}
-   *(Based on a simulated {consumer_cltv_metrics['total_users_considered']} users)*

**Note on Consumer Metrics:** For a true assessment of recommender system impact on churn and CLTV, a long-running A/B test is required where different user groups are exposed to different recommendation strategies, and their subsequent long-term behavior (churn, purchases leading to CLTV) is tracked.
