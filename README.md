# A/B Testing: Landing Page Conversion Analysis

## Objective
Investigate whether an updated landing page produces a different conversion rate from the original page using a historical e-commerce A/B testing dataset.

## Dataset
Udacity A/B testing educational dataset (~294,478 records), mirrored on [Kaggle](https://www.kaggle.com/datasets/zhangluyuan/ab-testing). Columns: `user_id`, `timestamp`, `group`, `landing_page`, and `converted`. The notebook fetches a public GitHub-hosted CSV; if it fails, download the CSV manually from Kaggle.

## Tools
Python, Pandas, NumPy, Matplotlib, Statsmodels, Google Colab / Jupyter Notebook.

## Method
1. Inspect rows, columns, missing values, and group/page inconsistencies.
2. For this educational per-protocol comparison, remove group/page mismatches and retain one row per user. This is **not** an intention-to-treat analysis.
3. Compute and visualize conversion rates.
4. Run a two-sided two-proportion Z-test and 95% Newcombe confidence interval for the difference.
5. Assess statistical and practical significance, and discuss limitations.

## Results
**To complete after running the notebook:**
- Control conversion rate: ___%
- Treatment conversion rate: ___%
- Difference (treatment minus control): ___ percentage points
- Two-sided p-value: ___
- 95% confidence interval: [___, ___] percentage points
- Recommendation: ___

## Important limitations
This is a historical educational dataset. Group/page mismatches and duplicate user IDs complicate causal inference. Assignment-based intention-to-treat analysis is preferred when original randomized assignments are reliable. Randomization and independence assumptions are not independently verified. Results are not a real-world deployment recommendation.

## How to run
Open `ab_testing_analysis.ipynb` in Google Colab or Jupyter and run cells from top to bottom. Install dependencies with `pip install -r requirements.txt` if needed.

## Future improvements
Pre-experiment power analysis, sample-ratio mismatch checks, time trends, and a preregistered decision threshold.
