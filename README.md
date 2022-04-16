# MechaCar_Statistical_Analysis
Using R to design a linear model that predicts mpg and perform t-tests on suspension coils.

### Purpose:
In this challenge, we are helping our data analytics team do the following:
  * Performing multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
  * Collecting summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
  * Run t-tests to determine if the manufacturing lots are statistically different from the mean population
  * Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you'll write a summary interpretation of the findings.
  
# Deliverable 1: Linear Regression to Predict MPG

Our dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using our knowledge of R, we designed a linear model that predicts the mpg of MechaCar prototypes using several variables from our data set.

## Summary of Linear Regression model

  * A summary of the linear regression can be displayed to determine the quality of the dataset. In this distribution of the residuals, the dataset fits in with the normal parameters, where the absolute value of the min and max are comparable |-19.47|~|18.58| and the median -.07 is close to zero.
  
  ![Summary of Linear Regression](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/summary_lm_del1.png)
  
### 1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

 - The variables that provided a non-random amount of variance to the mpg values in the dataset were "vehicle_length" and "ground_clearance."

### 2. Is the slope of the linear model considered to be zero? Why or why not?
 
 - The p-value (5.35e-11) is much smaller than a significance level of 0.01 and is therefore highly significant. This means that the slope of the linear model is not considered to be zero because the statistical analysis provides sufficient evidence that the null hypothesis is not true.

### 3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

 - The linear model does predict mpg of MechaCar prototypes effectively as the r-squared value is 0.7149. This means that there is about a 71.5% chance that future data will be able to fit this model.
 
# Deliverable 2: Summary Statistics on Suspension Coils

## Manufacturing Lot Summary:
Below is the summary statistics of all of the manufacturing lots. The mean is 1498.78 for this sample and the population mean was determined to be 1500.

![lotSummary](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.png)

## Summary by Manufacturing Lot Number:

The means of the lot numbers are similar to the population mean and the sample mean.

![all lots](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/lot_summary.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The variance for the total manufacturing lot is 62 < 100, which is within the expected design specifications of staying under 100 PSI. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of 170 > 100 and does not meet the design specifications. Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively.

# Deliverable 3: T-Test on Suspension Coils

## T-test for all Lots
All Manufacturing Lots: p-value = .6028, alpha = .05
.60 > .05, which means the total manufacturing lot is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![t-testForAllLots](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/t_test_for_all_del3.png)

## T-test for Lot 1
Lot 1: p-value = 1, alpha = .05
1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![Lot1](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/lot1_del3.png)

## T-test for Lot 2
Lot 2: p-value = .6072, alpha = .05

.60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![Lot2](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/lot2_del3.png)

## T-test for Lot 3
Lot 3: p-value = .04168, alpha = .05
.04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

![Lot3](https://github.com/nayanbarhate/MechaCar_Statistical_Analysis/blob/main/Images/lot3_del3.png)

## Study Design: MechaCar vs Competition
* One of the most important factors that consumers consider when looking for a new car is the safety rating. It would be useful to perform a statistical study to compare the safety ratings of MechaCar vehicles against the safety ratings of vehicles from other manufacturers. 

* The null hypothesis would be that MechaCar vehicles do not have statistically significant higher safety ratings than that of vehicles from other manufacturers, while the alternative hypothesis would be that MechaCar vehicles do have statistically significant higher safety ratings than that of vehicles from other manufacturers. 

* The way to test this would be to use a one-tailed t-test which would determine if there is any difference between the groups being compared. We would not use a two-tailed t-test as we have a prediction about the direction of the difference.

* The data needed to run the statistical test is a table of MechaCar vehicles and their respective safety ratings, along with various other manufactureres and their cars with safety ratings.
