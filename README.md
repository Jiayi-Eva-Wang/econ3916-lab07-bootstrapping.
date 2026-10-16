# econ3916-lab07-bootstrapping.

# Estimation & Bootstrapping — Quantifying Uncertainty Without a Formula

## Objective

In this lab, I learned how to measure uncertainty in statistical estimates using standard errors, confidence intervals, and bootstrapping.

## Methodology

- Loaded the UCI Adult Census Income dataset with 32,561 respondents.
- Compared standard deviation (SD) and standard error (SE) across different sample sizes.
- Used the Central Limit Theorem (CLT) to construct 95% confidence intervals.
- Applied bootstrapping by hand and with `scipy.stats.bootstrap`.
- Compared percentile and BCa confidence intervals.
- Used bootstrapping to compare mean weekly working hours between men and women.
- Tested an AI-generated bootstrap function and revised the prompt to make the results reproducible.

## Key Findings

- The standard deviation of age was 13.640 years, while the standard error for samples of 100 was approximately 1.36 years. Increasing the sample size reduced the SE.
- The CLT worked faster for age than for capital gains because capital gains were more heavily skewed.
- The bootstrap SE for median age was 0.0000, with a confidence interval of [37, 37]. This happened because many observations had the same age, keeping the median unchanged across resamples.
- For positive capital gains, the mean was $12,939 and the median was $7,298, showing a strongly right-skewed distribution.
- The bootstrap 95% percentile interval for mean capital gains was [$12,114, $13,780].
- Men reported an average of 42.43 working hours per week, compared with 36.41 hours for women. The estimated difference was 6.02 hours, with a 95% BCa confidence interval of [5.73, 6.28].
- After adding a random seed to the AI-generated function, I reproduced the Step 10 interval of [$12,173, $13,796].

## Conclusion

This lab helped me understand the difference between variation in data and uncertainty in estimates. I also learned that bootstrapping can estimate uncertainty without a simple formula, but its results depend on the data and sampling method.
