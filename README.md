# Multivariate OLS — What "Controlling For" Actually Does

## Objective
The objective of this lab was to understand how adding control variables affects OLS regression estimates, including omitted variable bias, collider bias, multicollinearity, and interaction effects.

## Methodology
- Simulated wage data to examine how leaving out ability affects the estimated return to education.
- Compared regressions with and without ability and used the omitted variable bias formula to calculate the expected bias.
- Applied the Frisch-Waugh-Lovell (FWL) theorem by removing the variation explained by ability from both wages and education, then comparing the result to the full regression.
- Tested how controlling for a collider can introduce bias into a regression.
- Examined multicollinearity by comparing coefficient estimates, standard errors, and variance inflation factors (VIF).
- Used an interaction term to estimate how the return to experience differs between union and non-union workers.
- Used AI to generate a specification-table function, revised my prompt to clarify missing-value handling, and checked the results against my original regressions.

## Key Findings
- **Omitted Variable Bias:** Without controlling for ability, the estimated return to education was $5,126, compared to the true value of $2,500. After controlling for ability, the estimate decreased to $2,546, much closer to the true effect.
- **Bias Formula:** The predicted omitted variable bias was $2,629, while the actual bias was $2,626, showing that the formula closely matched the simulation results.
- **Frisch-Waugh-Lovell Theorem:** Residualizing both wages and education with respect to ability produced the same education coefficient of approximately $2,546 as the full multivariate regression.
- **Collider Bias:** Controlling for a collider changed the estimated effect from approximately 0.001 to -0.596, even though the true effect was zero. The p-value was reported as 0.000, showing how controlling for the wrong variable can create a statistically significant but misleading result.
- **Multicollinearity:** High correlation between explanatory variables increased standard errors by approximately 12 times, making individual coefficients less precise without necessarily making the estimates biased.
- **Interaction Effects:** An additional year of experience was associated with approximately $903 in higher pay for non-union workers and $504 for union workers, showing that the return to experience differed between the two groups.
- **AI-Assisted Analysis:** Both versions of the AI-generated specification-table function matched the coefficients and standard errors from my original regressions. The revised prompt made the instructions clearer by specifying how missing values should be handled without changing the original dataset.
