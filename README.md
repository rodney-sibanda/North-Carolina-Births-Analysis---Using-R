# North-Carolina-Births-Analysis---Using-R

# Problem Statement 

- We are interested in investigating the relationship between birthweight of the baby and the race of the mother.

# Data Set

In 2004, the state of North Carolina released to the public a large data set containing information on births recorded in this state. This data set has been of interest to medical researchers who are studying the relation between habits and practices of expectant mothers and the birth of their children. This is a random sample of 1,000 cases from this data set

- The variables included in the dataset are:

    - fage - Father's age in years.
    - mage - Mother's age in years.
    - mature - Maturity status of mother
    - weeks - Length of pregnancy in weeks.
    - premie - Whether the birth was classified as premature (premie) or full-term.
    - visits - Number of hospital visits during pregnancy.
    - gained - Weight gained by mother during pregnancy in pounds.
    - weight - Weight of the baby at birth in pounds.
    - lowbirthweight - Whether baby was classified as low birthweight (low) or not (not low).
    - gender - Gender of the baby, female or male.
    - habit - Status of the mother as a nonsmoker or a smoker.
    - marital - Whether mother is married or not married at birth.
    - whitemom - Whether mom is white or not white.

# Downloading and working with 

![image](https://user-images.githubusercontent.com/126027138/221380927-e1ff6758-edd1-4725-9b0f-e78da8b5f2ca.png)

![image](https://user-images.githubusercontent.com/126027138/221380952-866bda92-ea9c-4ae6-abb3-0a63b3885052.png)

# Plot of Birthweight

![image](https://user-images.githubusercontent.com/126027138/221381059-2da85949-6462-4977-9b9d-3e6ae406270a.png)

- Plotted using weight (response) against mother's race, whitemom (explanatory)
- There does appear to be an association between birthweight and the race of the mother. The weight of babies born to white mothers tend to be greater than the weight of babies born to non white mothers. The median weight is slightly higher for white mothers and the boxplot is shifted slightly higher.

# Linear Model 

![image](https://user-images.githubusercontent.com/126027138/221381235-ba5597cc-4b04-4fa7-a17b-35cd3af16c68.png)

- created using whitemom rate as the predictor (explanatory) and weight as the response.
- The coefficient for whitemomwhite is 0.53092, which means that, on average, babies born to white mothers weigh 0.53092 more than babies born to non-white mothers.
- With a p-value of 4.44e-07, which is less than 0.05, indicates that the birthweight of babies born to white mothers is significantly different from the birthweight of babies born to non-white mothers
- The R-squared value of 0.02528 indicates that only 2.5% of the variability in birthweight can be explained by the race of the mother, which is a relatively weak relationship

Therefore, we can conclude that there is a statistically significant relationship between the birthweight of the baby and the race of the mother, with babies born to white mothers being, on average, slightly heavier than babies born to non-white mothers. However, the effect size is small, and other factors, such as the health status of the mother, may play a more significant role in determining birthweight.

# Confidence Interval for 𝛽<sub>1</sub>

![image](https://user-images.githubusercontent.com/126027138/221381675-770b6d5a-4451-465c-831d-1c239e1d51c2.png)

- The 95% confidence interval for 𝛽<sub>1</sub> is 0.326 to 0.736. In the context of this study, we are 95% confident that babies born to white mothers have a birthweight that is between 0.326 pounds and 0.736 pounds greater on average than babies born to nonwhite mothers. Therefore, mother's race is a statistically significant predictor of birthweight

# Residual Plot

![image](https://user-images.githubusercontent.com/126027138/221381864-3ba1304f-d3bc-4e88-a6ba-ee1453fd0d99.png)

- The histogram of the residuals is roughly bell shaped which suggests that the assumption of normally distributed errors is appropriate. 

# Conclusions

We can conclude that there is a statistically significant relationship between the birthweight of the baby and the race of the mother, with babies born to white mothers being, on average, slightly heavier than babies born to non-white mothers. The linear regression analysis shows that the coefficient for whitemomwhite is 0.53092, which is statistically significant at the 0.05 level, with a p-value of 4.44e-07. However, the magnitude of the relationship is small, and other factors, such as the health status of the mother, may play a more significant role in determining birthweight.

Additionally, the histogram of the residuals is roughly bell-shaped, which suggests that the assumption of normally distributed errors is appropriate for the linear regression model that has been fitted to the data. This implies that the linear regression model is a valid model, and the conclusions drawn from the analysis are reliable and trustworthy.

Overall, the findings suggest that while the race of the mother may have a statistically significant effect on the birthweight of the baby, it is likely not the only factor that contributes to birthweight, and further research is needed to understand the complex relationships between maternal health, socio-economic status, and other factors that may influence birthweight.

