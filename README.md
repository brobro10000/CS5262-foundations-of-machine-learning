# CS5262 Foundations of Machine Learning

## Performance Metrics for the Adult Income Dataset

The Adult Income Dataset can be used to evaluate and optimize sales lead targeting by predicting whether an individual earns more than $50K annually. This classification task allows businesses to allocate resources more effectively by identifying high-value to potentially lead to higher revenue per sale.

### Classification Outcomes and Associated Costs/Benefits

The outcomes of the classification model can be interpreted as follows:

|  Outcome | Hypothetical Sales Interpretation |  Hypothetical Associated Cost/Benefit |
|------------------------|----------------------|-------------------------|
| True Positive (TP)     | Correctly identified high-value lead; converted into a sale. | Profit per sale |
| True Negative (TN)     | Correctly identified low-value lead; avoided wasted effort. | Neutral or small cost savings |
| False Positive (FP)    | Misclassified a low-value lead as high-value; wasted sales resources. | Cost per wasted effort |
| False Negative (FN)    | Missed a high-value lead by classifying them as low-value. | Opportunity cost |

### Hypothetical Example

A confusion matrix example demonstrates the distribution of leads based 1000 potential leads based on hypothetical predicted values of the adult income model:

|                        | Predicted: High-value Lead | Predicted: Low-value Lead |
|------------------------|----------------------------|---------------------------|
| **Actual: High-value** | 300 (TP)                    | 75 (FN)                   |
| **Actual: Low-value**  | 125 (FP)                    | 500 (TN)                  |

**Cost/Benefit Analysis:**

Adding hypothetical cost and revenue to each category, we can hypothesize which metric we would choose to optimize when creating and modifying our predictive model. 


| Metric                 |  Value per outcome in dollars |
|------------------------|----------------------|
| True Positives (TP)    |  $500      |
| True Negatives (TN)    |   $50      |
| False Positives (FP)   | ($200)      |
| False Negatives (FN)   | ($400)      |

Based on the table above and 1000 potential leads we can determine the cost. 

- **True Positive (TP):** 300 × 500 = $150,000
- **True Negative (TN):** 500 × 50 = $25,000
- **False Positive (FP):** 125 × ($200) = ($25,000)
- **False Negative (FN):** 75 × ($400) = ($30,000)

Based on these predictive outcomes and their respective value we can determine our potential sales.

**Potential Total Sales Impact:**

To determine the hypothetical sales impact of 1000 leads, we sum up all values from the confusion matrix.

- **Net Gain:** TP + TN + FP + FN = 150,000 + 25,000 - 25,000 - 30,000 = $120,000

### Optimization Strategies

We've determined based on our predictive model and 1000 leads, we can isolate which variables to maximize and minimize to return the most benefit financially based on our model. Based on our cost benefit analysis, we've determined that increasing the true positive value (sensitivity) and decreasing false negatives will have the largest impacts, while false positives and true negatives cancel each other out. But, reducing false positives will increase the overall precision of our model, so it cannot be ignored in this scenario.

### In summary:

To maximize sales impact, we can optimize our model performance and thus improve overall revenue by:
- **Increasing Precision:** Reducing false positives to avoid wasting resources on low-value leads.
  - Precision = TP / (TP + FP)
- **Increasing Recall:** Reducing false negatives to ensure fewer high-value leads are missed.
  - Recall = TP / (TP + FN)
