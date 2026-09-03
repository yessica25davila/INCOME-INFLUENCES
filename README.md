# Income Influences: A Logistic Regression Analysis

UCI CENSUS DATA (1994) Oregon State University-Capstone Project | April 2025 - June 2025

This analysis investigates the relationship between demographic and employment factors using 1994 U.S. Census data. The main goal was to understand how factors influenced whether someone earned over $50k annually. I used logistic regression on a dataset from the Machine Learning Repository maintained by the University of California, Irvine (UCI). 

Why does this matter? This kind of analysis can help guide policies and decisions that aim to promote fairness and efficiency in the labor market. It highlights the role that work hours — and persistent gender differences — can play in income outcomes. 

I focused on two key questions: First, is there an association between how many hours someone works per week and whether they earn over $50,000 — after accounting for other variables? Findings from the initial exploratory data analysis revealed that most of the individuals in the dataset earned $50,000 or less as seen in the scatterplots below.  The findings were broken down by gender, which showed that males, on average, worked more hours per week than females. There is a visible concentration around 40 hours worked per week among both genders in the first plot and a possible trend where individuals with more years of education could be more likely to make more than $50,000 in the second plot.


<img width="360" height="223" alt="Screenshot 2026-03-13 at 2 03 45 PM" src="https://github.com/user-attachments/assets/d00ead16-303b-4484-9576-f4ad34b67fe3" />
<img width="358" height="223" alt="Screenshot 2026-03-13 at 2 03 53 PM" src="https://github.com/user-attachments/assets/f01b7e95-4b6d-44b4-94a8-98bfbadf7e82" />

During the model fitting process, the variable hours-per-week was not included in the first model. Although several variables were significant, our main interest was understanding the effect of hours worked. When hours-per-week was added in the second model, it had a strong and statistically significant effect (p < 0.001). The coefficient was 0.02949, which corresponds to an odds ratio of 1.03 with a 95% confidence interval from 1.026 to 1.033.

The results show that hours worked per week is significantly related to earning more than $50,000 per year. After accounting for other variables, each additional hour worked increases the odds of earning over $50,000 by about 3% (or 1.03 times) compared to someone who works one hour less. 

For the second question of interest, After accounting for age, is there evidence of a difference in the earnings probability of men and women? Regarding the second research question, the model revealed a clear disparity in income between men and women, even after adjusting for age. Males had an estimated probability of 31% of earning over $50,000, while females had an estimated probability of just 11%. The odds ratio for men compared to women was 3.17, meaning that men had more than three times the odds of earning over $50,000 than women of the same age. A plot of income probability by age and sex demonstrated an increasing trend in income with age for both sexes, though males consistently had higher probabilities across all age groups.

<img width="480" height="296" alt="Screenshot 2026-03-13 at 2 19 22 PM" src="https://github.com/user-attachments/assets/38345a46-830e-42c5-85b4-2a5a08172f2c" />


While the data is from 1994 and may not reflect today’s workforce perfectly, the overall takeaway remains relevant: data-driven insights can help us better understand income disparities and improve employment practices going forward
