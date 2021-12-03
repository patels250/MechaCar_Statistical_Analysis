# MechaCar_Statistical_Analysis

## Overview

MechaCar, AutosRU's newest prototype, is suffering from production troubles that are costly and run the risk of failing the team's deadlines.

The purpose of this analysis is to review production data for insights that may help circumvent manufacturing risks.

## Linear Regression to Predict MPG

Before moving on to Linear Regression, we take a look at the Correlation Coefficient Matrix to identify variables of interest. There are no variables that share what is considered a strong correlation (1>= absolute value "r" >= 0.7), as revealed by the matrix.

### Correlation Coefficient Matrix Highlights

- "MPG" and "Vehicle Length" share a moderate correlation of 0.61, which is the strongest of all variables, with "MPG" and "Ground Clearance" coming in second at a weak-moderate correlation level of 0.33.
- When we square the Vehicle Length coefficient, we get R-squared of approximately 0.37. This indicates that Vehicle length will only predict about 37% of mpg observations.

We should run a Multiple Linear Regression model to test for more prediction reliability.

### Multiple Linear Regression Highlights

- According to our results, vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model. In other words the vehicle length and ground clearance have a significant impact on mpg.
- In addition, the p-value of our linear regression analysis is 5.35e-11, which is much smaller than our assumed significance level of 0.05%. Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.
- R-squared of approximately 0.71. This indicates that the multiple linear regression will predict 71% of mpg observations.

## Summary Statistics on Suspension Coils

The design specification for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI). We want to confirm that the manufacturing data meets this design specification for all manufacturing lots in total and each lot individually.

Weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots in the Suspension_Coil.csv dataset. The dataset is comprised of the PSI metric for 150 vehicles produced at 3 lots.

Initially, we are inclined to believe that lot 3 is doing something wrong, as it is the only lot that exceeds the 100lb weight capacity. However, looking at the Median and Mean, we can see that the data is Left Skewed which indicates there is a higher probability that lower weights exist at this location than others. This is evidenced by the Standard Deviation being higher for this location as well.

We recommend that the manufacturing team revisit its approach with vehicle allocation to these lots in order to normalize distributions so they each meet the design specifications.

## T-Tests on Suspension Coils

We want to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. Using our knowledge of R, we will perform t-tests to calculate the p-value and compare it against a significance level of 0.05.

### All Manufacturing lots

At a significance level of the common 0.05 percent, our p-value of 0.06 is above the significance level. Therefore, we do not have sufficient evidence to reject that there is a statistical difference between All Manufactuting lots and the population mean. The two means are statistically similar.

### Lot 1

At a significance level of the common 0.05 percent, our p-value of 1.0 is above the significance level. Therefore, we do not have sufficient evidence to reject that there is a statistical difference between Lot 1 and the population mean. The two means are statistically similar.

### Lot 2

At a significance level of the common 0.05 percent, our p-value of 0.61 is above the significance level. Therefore, we do not have sufficient evidence to reject that there is a statistical difference between Lot 2 and the population mean. The two means are statistically similar.

### Lot 3

At a significance level of the common 0.05 percent, our p-value of 0.042 is below the significance level. There is sufficient statistical evidence to reject that there is a statistical difference between Lot 3 and the population mean. The two means are statistically different.

## Study Design: MechaCar vs Competition

In order to ensure the new MechaCar prototype is a success, we should evaluate how it stands up to the competition. Lets design a potential study that will provide statistical insight to how the MechaCar performs vs competition.

### Metrics

The metrics to test are both city and highway fuel efficiency.

### Hypothesis

Null: MechaCar has the same fuel efficiency for each cylinder class. Alternate: MechaCar does not have the same fuel efficiency for each cylinder class.

### Statistical Tests

I would use linear regression and 2 Sample T-Tests to test the hypothesis against the population mean for each metric.

### Data

Gathering the proper variables is a great start to our analysis.

I recommend the following data variables: Manufacturer (mfg) Engine Size (cyl) Highway Fuel Efficiency (hwy) City Fuel Efficiency (cty) Model Year Cost