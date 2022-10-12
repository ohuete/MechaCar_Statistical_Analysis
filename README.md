# MechaCar Statistical Analysis
## Purpose and Background
In this project, I performed multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes, collected summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots, ran t-tests to determine if the manufacturing lots are statistically different from the mean population, designed a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. This project was completed using R. 

## Linear Regression to Predict MPG
Below is a screenshot of the linear regression model which is used to determine the coefficients of the dataset. 

![Screen Shot 2022-10-08 at 10 40 28 PM](https://user-images.githubusercontent.com/107595127/195435991-2ff4252e-dccc-4670-98b7-24d2e1c329ae.png)

### Summary of Linear Regression
R generates a summary of the linear regression model which then tells us key details/information of the dataset. The linear regression model tells us how each variable impacts the topic of interest, in this case, MPG. The model tells us how each factor interacts and influences one another to make useful conclusions. In this output, our paramters and median is given. We are dealing with parameters of -19.47(min.) and 18.58(max.) with a median of 0.06. 

After taking a look at the *p-value*, we can infer that the strongest influencers and contributers of non-random variance are vehicle length and ground clearance. 

While our median value is close to zero, the slope of the linear model is not exactly zero. The value of the coefficeints are not exactly zero and they also have significnant p-values. 

Also, the R-squared value is .7149, indicating that the data is indeed effective when predicting MPG of MechaCar prototypes. 

## Summary Statistics on Suspension Coils
Below are images of our summary statistics on Suspension Coil. First we have the total summary then the Lot summary. 

<img width="344" alt="Screen Shot 2022-10-11 at 12 44 05 PM" src="https://user-images.githubusercontent.com/107595127/195437668-af25020a-fd56-475b-88ff-01f87f04d947.png">

<img width="503" alt="Screen Shot 2022-10-11 at 12 43 55 PM" src="https://user-images.githubusercontent.com/107595127/195437701-04ba6118-1e32-4db8-a58d-1c823f377f4a.png">

Considering the maximum variance of 100 PSI, the total summary dataframe shows that the overall results of the three lots have a variance that fall below the maximum. Overall, the variance value is 62 PSI. When we look at the lots individually, Lots 1 and 2 have a variance of .9 and 7 while Lot 3 exceeds the design specifications with variance value of 170 PSI. 

## T-Tests on Suspension Coils

![Screen Shot 2022-10-12 at 1 25 10 PM](https://user-images.githubusercontent.com/107595127/195440874-73a2b588-0023-4c5b-93e1-f380c4b32999.png)

The t-test ran for all lots show that the overall p-value is 1, meaning there is statistical insignificance and therefore we must retain the null hypothesis. Similar to the summary statistics and the dataframes, Lots 1 and 2 show significant p-values and we can reject the null hypothesis. Again, Lot 3 holds an insignificant value and in that case we must retain the null hypothesis. 

## Study Design: MechaCar vs Competition
When comparing the performance of MechaCar and other competitors, we must take into account consumer interests. For instance, we have taken into account MPG but we can also consider horespower, safety specs, engine durability, cost, etc. Considering the factors of interest, we can run similar tests as we did for MPG. 

For these factors, we can create a null hypothesis that states there is not difference in the MechaCar with competitors. The alternative hypothesis will of course then be that the MechaCar is different and arguably better. To do so, we will again perform a one-tailed t-test to determine the values of each factors and take note of value direction. To run the test, we would of course need to obtain data of the said factors from both MechaCar and the competitors. 
