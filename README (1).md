# Television and Short-Term Attention: A Matched-Pair Randomized Experiment

A pre-registered, matched-pair randomized experiment testing whether 30 minutes of TV changes immediate attention compared with sitting quietly. Course project for UCLA Stats 101B, run on a simulated population (the fictional city of Colmar). Analysis in R.

**Full report:** [`Stats101B_Final_Report.pdf`](Stats101B_Final_Report.pdf)

## Question

Among the adults enrolled, what is the effect of watching TV for 30 minutes, compared with sitting still for 30 minutes, on the number of items missed on an attention test given right afterward?

## Design

- **Treatment:** one factor, two levels: watch TV for 30 min vs. sit still for 30 min
- **Response:** items missed on an attention test (higher = worse attention)
- **Recruitment:** random household selection, then a random adult within the household; 122 consenting participants
- **Matching:** everyone took a baseline attention test, participants with similar scores were paired, and one person in each pair was randomly assigned to each treatment
- **Primary comparison:** within-pair difference in final scores (TV − Sitting)

**Power analysis.** The original target of 226 participants wrongly used an independent-samples calculation. Before looking at any outcome data, it was corrected to a paired design: smallest meaningful difference of 4 items, planning SD of 10.65 for within-pair differences, α = 0.05, 80% power. That required 58 pairs, or **116 participants**.

## Results

Three participants withdrew after assignment, so their pairs were dropped. The analysis used **58 complete pairs (116 participants)**.

| | Mean items missed | SD |
|---|---|---|
| Sitting | 15.64 | 13.44 |
| TV | 17.10 | 15.42 |

- **Mean within-pair difference (TV − Sitting): +1.47 items** (SD = 9.94, SE = 1.30)
- **95% CI: (−1.15, 4.08)**
- Paired t-test: t(57) = 1.12, p = 0.266. The equivalent block-adjusted ANOVA gave F(1, 57) = 1.26, p = 0.266.

**Conclusion: inconclusive, not "no effect."** The result was not statistically significant, but the confidence interval includes the prespecified meaningful worsening of 4 items, so the experiment cannot rule out a meaningful harm to attention.

## Diagnostics and deviations

- Residual plots and the Q-Q plot looked reasonable, with the largest |standardized residual| at 2.69. Residual variance rose somewhat with fitted values, so the constant-variance assumption may not hold perfectly.
- The sample size was amended (226 → 116) before any confirmatory analysis.
- 71 responses were collected on Aug 30, one day after the registered Aug 29 deadline.

## Limitations

- Testing happened at slightly different times of day, which could add noise from fatigue
- The sample was not a probability sample, so results should not be generalized beyond the enrolled participants
- Only the immediate effect was measured, not longer viewing or delayed effects

## Files

- `Stats101B_Final_Report.pdf`: full write-up with figures, ANOVA table, and diagnostics

## Credits

Team project for UCLA Stats 101B with Nathan Goldstein, Jonathan Pak, Kalani Caetano, and Yitie Ge. My contributions: design, allocation, protocol, and power analysis (with Nathan); data audit, deviations, and descriptive summaries (with Kalani and Yitie); checking the data, reported results, and analysis file.
