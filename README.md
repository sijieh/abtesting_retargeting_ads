# 📊 A/B Testing on Retargeting Ads: Analysis and Optimization

This project analyzes the effectiveness of a retargeting ad campaign using a randomized A/B testing framework. The goal is to identify whether retargeting increases customer spending and to develop a data-driven policy that maximizes profit by targeting only the most responsive customers.

---

## 🧠 Project Workflow

### 1. A/B Test Design & Validity Check

I began by randomly splitting customers into treatment and control groups. Only the treatment group was eligible for retargeting ads. To ensure the test was valid:
- I verified balanced group sizes.
- I confirmed similar distributions of customer characteristics (e.g., site visit patterns) across groups.

### 2. Analyze Campaign Impact

I explored the distribution of customer spending to understand the general patterns and detect skewness. The average spend was compared between treatment and control groups. A statistical significance test (e.g., t-test) was conducted to evaluate whether the difference in spending was meaningful.

### 3. Estimate Individual Treatment Effects (CATE)

I built a regression model that includes the treatment indicator and its interactions to estimate Conditional Average Treatment Effects (CATE) at the individual level. This allowed me to:
- Predict how much each customer would spend with and without treatment.
- Understand heterogeneity in treatment effects across the customer base.

### 4. Validate CATE Predictions

CATE scores were grouped into bins, and average lift was calculated per bin to assess whether higher scores correlate with higher incremental impact. This helped validate the model’s usefulness in identifying high-value targets.

### 5. Develop an Optimal Targeting Policy

Using predicted CATE scores, I created a policy that only retargets customers whose expected incremental value exceeds the campaign cost. This policy was compared against two benchmarks:
- Retargeting no one
- Retargeting everyone

The comparison was based on expected profit and targeting efficiency.

### 6. Evaluate Ads Exposure Effects

I analyzed differences in spend between customers who were actually exposed to ads versus those who were not. This accounted for real-world delivery variability and highlighted how exposure is often biased toward high-value customers.

### 7. Bid Strategy Optimization

Based on observed ad exposure effects and expected margins, I estimated optimal bid prices using a margin-adjusted model. A customer-level approach was also proposed to further personalize bidding strategies.

---

## ✅ Key Takeaways

- Retargeting is effective but not uniformly so across all customers.
- CATE modeling enables personalized targeting to maximize efficiency and return.
- Selective retargeting outperforms blanket campaigns in profitability.
- Bidding strategies can be optimized using modeled customer responsiveness.
