Project Overview:
•	The purpose of this project was to perform retrospective analysis of historical data, analytical verification of current automotive specifications, and study design of future project testing, as part of the data analytics team at AutosRUs using the programming language R. 
•	The analysis must be based on a statistical backbone, a quantitative metric, with a clear interpretation of the results. The analysis required a production of the summary statistics of different variables, visualizations of different data sets, and finally our own interpretation of the statistical test results. 

Purpose:
The purpose of this challenge was to help Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team in production of AutosRUs’ newest prototype, the MechaCar. 
The MechaCar is currently suffering from production troubles that are blocking the manufacturing team’s progress, and upper management has directed Jeremy and his team to assist.
In this challenge, we were tasked to assist Jeremy and the data analytics team do the following:
•	Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
•	Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
•	Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
•	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

Deliverable 1 – Linear Regression to Predict MPG:
•	Ground clearance and vehicle length and to a lesser extent vehicle weight are statistically unlikely to provide random amounts of variance to the linear model, meaning that all three coefficients have a significant impact on miles per gallon (mpg) for the MechaCar protypes. This is based on the probability coefficient (Pr(>|t|) value being smaller for the ground clearance, vehicle length, and vehicle weight variables. The other variables, spoiler angle and AWD, do appear to contribute a random amount of variance to the linear model, which is presented in their probability coefficient being larger.
•	The slope of the linear model is not considered to be 0. This is because the p-Value which measures the probability that a particular statistical measure will be greater than or equal to 0, or more simply, tells us the likelihood that we would see similar results if we tested our data again, is calculated to be 5.35e-11. The p-value of 5.35e-11 is significantly smaller than the assumed (normal) p-value of 0.05. What this means is that the probability of being wrong that these variables are random is extremely unlikely.
•	The linear model does predict miles per gallon (mpg) effectively approximately 71.4% of the time. This is based on the calculated r-squared value, which in this case was 0.7149, which represents how well the regression model represents real world data, falling between a range of 0 and 1, where 0 represents no predictability, and 1 represents complete predictability. In this case, the r-squared value of 0.7149 demonstrates the strength of the correlation to be strong.
![image](https://user-images.githubusercontent.com/93049541/154872187-7cb3ffdd-701d-4ae8-8747-84543439d23d.png)
https://github.com/sachinnabar/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%201.PNG

Deliverable 2 - Summary Statistics on Suspension Coils:
•	The design specifications for the MechaCar suspension coils dictated that the variance of the suspension coils must not exceed 100 pounds per square inch. Based on the total_summary dataframe that was created, we can see that the variance total variance for all three lots was 62.29356, which falls well below the 100-psi threshold.
•	 Based on a per lot basis however, we can see in the lot_summary dataframe, that the variance does differ by lot number. Lot 1 and Lot 2 have a variance of 0.9795918 and 7.4693878 respectively, which both fall within the variance tolerance of 100-psi. Lot 3 however has a appreciably higher variance of 170.2861224, which exceeds the variance toleration dictated in the design specifications. This means that Lot 3 will have to be removed for production implementation, but Lot 1 and Lot 2 could be used in production.

Total_Summary Table
![image](https://user-images.githubusercontent.com/93049541/154873607-298cc9ce-2bee-4985-8fec-be3110d6db5f.png)
https://github.com/sachinnabar/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%202.1.PNG

Lot_Summary Table
![image](https://user-images.githubusercontent.com/93049541/154873629-e4cbc5f7-7406-4984-8529-521bef880b66.png)
https://github.com/sachinnabar/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%202.2.PNG

Deliverable 3 - T-Tests on Suspension Coils
•	Based on the combine lot t-test, we can see that the p-value is equal to 0.06028 which is larger than the normal significance level of 0.05, suggesting that there is no significant linear relationship and that the effect the PSI has is based on random chance and error. 
•	This means that the null hypothesis must be accepted (the null hypothesis is failed to be rejected) as there is not enough evidence to support its rejection.
Combined Lot T-Test
![image](https://user-images.githubusercontent.com/93049541/154874846-75d91d6e-8f07-4b01-b903-4ebe96e7644f.png)
https://github.com/sachinnabar/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%203.1.PNG

Individual Lot T-Test

•	Lot 1 
The p-value for Lot 1 is equal to 1, signifying an extremely strong correlation between the Lot 1 PSI and the population mean of 1500-psi. This is further supported by the fact that the Mean PSI for Lot 1 was itself 1500, demonstrating that there is no statistical difference between the sample of Lot 1 and the population mean.
•	Lot 2 
The p-value for Lot 2 is equal to 0.6072, once again signifying a strong correlation between the Lot 2 PSI and the population mean of 1500-psi. The Mean PSI for Lot 2 was 1500.20, which is almost coequal to the population mean of 1500. Similar to Lot 1, we must fail to reject the null hypothesis.
•	Lot 3 
Lot 3 presents a different representation than the first two lots. In varies significantly different from the results for Lot 1 and Lot 2. It has impacted the overall p-value for the combined lots, which is evidenced by the fact that it had dramatically larger variance than the other two lots. Based on the p-value presented of 0.04168, we must reject the null hypothesis as the evidence suggests that there is a very weak correlation between the sample PSI of Lot 3 and the population mean.
![image](https://user-images.githubusercontent.com/93049541/154874901-bf4b3bf7-1b56-4069-a815-5af11ef0c6d5.png)
https://github.com/sachinnabar/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%203.2.PNG



