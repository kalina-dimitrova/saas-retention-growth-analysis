# SaaS user retention and growth analysis (synthetic data)

An end-to-end analytics case study on a synthetic SaaS dataset, written as a practice project. It covers user behavior, retention, revenue and growth forecasting, with a focus on turning data into recommendations for product and business decisions.

## Key questions
- How is user adoption evolving over time?
- What drives retention and long-term value?
- Which customer segments are most valuable?
- Which onboarding approach performs better?
- What does future growth look like?

## Key insights
- **Adoption is growing steadily** with clear seasonality; daily active users increased about 3x over the observed period.
- **Usage is similar across segments, but revenue is not.** Enterprise accounts have roughly 5-13x higher tenure-weighted MRR than the other segments.
- **Onboarding approach B outperforms A**, with about 15% higher average adoption intensity (Welch's t-test, p < 0.001, Cohen's d of about 0.3, a small-to-moderate effect).
- **Growth is expected to continue.** The Q1 2026 forecast averages about 1,620 daily active users, and the upper end of the 95% prediction interval is near 1,950.

Full presentation: [Results_Presentation.pptx](./Results_Presentation.pptx)

## Business recommendations
- Prioritize enterprise acquisition and retention
- Roll out onboarding approach B across new users
- Plan infrastructure capacity with a buffer above the forecast's upper bound
- Monitor segment mix and pricing changes as key revenue drivers

## Project structure
- `Data_Analytics_Case_Study_synthetic_dataset.ipynb`: full analysis, including SQL queries, exploration, testing and forecasting
- `Results_Presentation.pptx`: executive summary of the insights and recommendations
- `data/`: the SQLite database used by the notebook (`gogosync_analytics.db`)
- `requirements.txt`: Python packages needed to run the notebook

## How to run
1. Install the packages: `pip install -r requirements.txt`
2. Make sure `data/gogosync_analytics.db` exists.
3. Open the notebook in Jupyter and choose Kernel, then Restart & Run All.

## Skills demonstrated
- SQL (CTEs, joins, window functions) and Python (pandas)
- Cohort and retention analysis
- A/B test evaluation with effect size
- Time series forecasting with holdout validation and prediction intervals
- Data storytelling and presentation

## Notes
- The dataset is **synthetic** and came with a take-home exercise. It is shared for portfolio purposes only, so the findings describe the synthetic data, not a real product.
- The forecast assumes stable growth and seasonality, and does not account for product launches, pricing changes or other structural shifts.
