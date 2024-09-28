# Hypothesis-Testing-with-Men-and-Women-Soccer-Matches
This project investigates whether more goals are scored in women’s international soccer matches compared to men's. By performing a statistical hypothesis test using official FIFA World Cup data, the analysis provides insights that may interest followers of both men's and women's international soccer.

---

# Hypothesis Testing with Men's and Women's Soccer Matches

<img src="https://images.unsplash.com/photo-1656501149035-4dea12229ab8?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="A soccer pitch for an international match" width="900"/>

Photo by [Krišjānis Kazaks](https://unsplash.com/@kazaks) on [Unsplash](https://unsplash.com).

<br>

## Introduction

This project investigates whether more goals are scored in women’s international soccer matches compared to men's. By performing a statistical hypothesis test using official FIFA World Cup data, the analysis provides insights that may interest followers of both men's and women's international soccer.

<!-- The analysis is carried out under the assumption that each match is independent, ignoring factors such as team form. The data used are from FIFA World Cup matches played since 2002. -->

## Research Question

> Are more goals scored in women’s international soccer matches compared to men’s?

To answer this, a hypothesis test at a 10% significance level would be conducted using the following hypotheses:

- **Null Hypothesis ($H_0$)**: The mean number of goals scored in women’s international soccer matches is the same as men’s.

- **Alternative Hypothesis ($H_A$)**: The mean number of goals scored in women’s international soccer matches is greater than men’s.

## Data

The project uses two datasets from [DataCamp](https://www.datacamp.com/):

- `men_results.csv`: Contains the results of every official men's international football match since the 19th century.
- `women_results.csv`: Contains the results of every official women's international football match since the 20th century.

### Key Data Columns

| Column         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `'date'`       | The date when the match took place (formatted as YYYY-MM-DD or DD/MM/YYYY).  |
| `'home_team'`  | The team that played on their home ground.                                  |
| `'away_team'`  | The team that played away from their home ground.                           |
| `'home_score'` | The number of goals scored by the home team.                                |
| `'away_score'` | The number of goals scored by the away team.                                |
| `'tournament'` | The type of competition or event where the match occurred (e.g., FIFA World Cup). |

For this analysis, only official FIFA World Cup matches (not including qualifiers) since **2002-01-01** are considered.

## Methodology

### Assumptions

- **Independence of Matches**: Each match is assumed to be independent of others. This means that team performance in one match does not influence future performance, ignoring factors such as winning streaks or tournament phases.

- **Tournament and Time Scope**: The analysis is limited to `FIFA World Cup` matches post-2002, `2002-01-01`, as performances and playing styles have evolved significantly over time.

### Statistical Test

Given the right-skewed nature of the data, the **Mann-Whitney U test** (a non-parametric alternative to the two-sample t-test) is used to compare the distributions of goals scored in men’s and women’s matches.

### Analysis Steps:

1. Load and filter data for FIFA World Cup matches since 2002.

2. Calculate the total number of goals scored per match for both men's and women's games.

3. Check for normality using histogram plots.

4. If the normality assumption doesn't hold: conduct the Mann-Whitney U test to compare the number of goals scored.

-   Otherwise, the homoscedasticity assumption should be checked as well. If it holds, a two-sample t-test should be conducted.

5. Determine the p-value and decide whether to reject or fail to reject the null hypothesis, using an $\alpha$ of 10%.

## Results

The analysis yielded the following results:

- **P-value**: 0.087344

- **Conclusion**: Based on a 10% significance level, the null hypothesis was **rejected**. 

This suggests that more goals are scored in women’s international soccer matches than men's.

## Visualization

The following histograms illustrate the right-skewed distribution of goals scored in both men's and women's FIFA World Cup matches:

![Men's Goals Distribution](https://github.com/MohamedMostafa259/Hypothesis-Testing-with-Men-and-Women-Soccer-Matches//blob/d27098b40bb41b528f39d8318618da5897723c72/visuals/MenDist.png)  

![Women's Goals Distribution](https://github.com/MohamedMostafa259/Hypothesis-Testing-with-Men-and-Women-Soccer-Matches//blob/d27098b40bb41b528f39d8318618da5897723c72/visuals/WomenDist.png)

## Future Improvements

- **Team Form Analysis**: Expand the analysis by considering team form (e.g., winning/losing streaks) to see how momentum impacts performance.

- **Time Series Analysis**: Investigate whether goal-scoring patterns have changed over time.

- **Additional Hypothesis Tests**: Explore other hypothesis tests, such as comparing scoring trends between different continents or specific teams.

