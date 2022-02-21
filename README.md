Project Overview
•	The purpose of this project was to perform retrospective analysis of historical data, analytical verification of current automotive specifications, and study design of future project testing, as part of the data analytics team at AutosRUs using the programming language R. 
•	The analysis must be based on a statistical backbone, a quantitative metric, with a clear interpretation of the results. The analysis required a production of the summary statistics of different variables, visualizations of different data sets, and finally our own interpretation of the statistical test results. 

Purpose
The purpose of this challenge was to help Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team in production of AutosRUs’ newest prototype, the MechaCar. 
The MechaCar is currently suffering from production troubles that are blocking the manufacturing team’s progress, and upper management has directed Jeremy and his team to assist.
In this challenge, we were tasked to assist Jeremy and the data analytics team do the following:
•	Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
•	Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
•	Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
•	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

Deliverable 1 – Linear Regression to Predict MPG
•	Ground clearance and vehicle length and to a lesser extent vehicle weight are statistically unlikely to provide random amounts of variance to the linear model, meaning that all three coefficients have a significant impact on miles per gallon (mpg) for the MechaCar protypes. This is based on the probability coefficient (Pr(>|t|) value being smaller for the ground clearance, vehicle length, and vehicle weight variables. The other variables, spoiler angle and AWD, do appear to contribute a random amount of variance to the linear model, which is presented in their probability coefficient being larger.
•	The slope of the linear model is not considered to be 0. This is because the p-Value which measures the probability that a particular statistical measure will be greater than or equal to 0, or more simply, tells us the likelihood that we would see similar results if we tested our data again, is calculated to be 5.35e-11. The p-value of 5.35e-11 is significantly smaller than the assumed (normal) p-value of 0.05. What this means is that the probability of being wrong that these variables are random is extremely unlikely.
•	The linear model does predict miles per gallon (mpg) effectively approximately 71.4% of the time. This is based on the calculated r-squared value, which in this case was 0.7149, which represents how well the regression model represents real world data, falling between a range of 0 and 1, where 0 represents no predictability, and 1 represents complete predictability. In this case, the r-squared value of 0.7149 demonstrates the strength of the correlation to be strong.
![image](https://user-images.githubusercontent.com/93049541/154872187-7cb3ffdd-701d-4ae8-8747-84543439d23d.png)
https://github.com/sachinnabar/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%201.PNG
