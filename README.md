# Cyclistic Bike-Share Conversion Strategy 🚲
---

## The Challenge: Converting Casual Riders to Annual Members


The core business goal for Cyclistic is to increase profitability by converting **casual riders** (Pay-As-You-Go) into **annual subscribers**.

My analysis aimed to identify key behavioral differences between the two user segments that could be leveraged for a data-driven marketing campaign.

---

## Key Data-Driven Insights

My analysis used **Generalized Linear Models (GLM: Gamma and Poisson)** and **Two-Way ANOVA** to model user behavior, revealing a critical opportunity:

1. The Value Difference: Duration vs. Frequency
- **Casual Riders** take significantly **longer, more valuable trips** (Average: 77 minutes) but ride far less often.
- **Annual Members** are high-frequency, **short-duration riders** (Average: 12 minutes).

2. The Behavioral Trigger: Weekends
- **ANOVA Insight**: There is a significant interaction between **User Type** and **Day of the Week** on ride duration (_F_(6, 790340) = 876.96, _p_< .001. ).
- **Implication**: Casual riders' long trips are primarily concentrated on weekends, suggesting they are **leisure** riders. Annual members' duration remains consistent throughout the week.

<p align="center">
  <img src="./Plots/Boxplot-Ride-Length-by-User-Type-and-Day-of-Week.png" alt="Ride Length by User Type and Day of Week" width="600"/>
  <br>
  <em>Figure: Ride length by user type and day of week</em>
</p>

---

## Actionable Recommendation
**Strategy**: Implement a marketing campaign that incentivizes the unique, high-value behavior of casual riders: **long ride duration**.

1. Tiered Discount Plan
- Create a discount on the annual membership based on a casual rider's **cumulative ride time** (e.g., 10% discount for logging 30+ minutes of total ride time, the modeled mean of high-value casual riders). This directly rewards the behavior most valuable to Cyclistic's service.
  
- **Refinement**: Focus the campaign solely on the **ride duration metric**, as using a 'total rides' limit is impractical for individual customer targeting.

2. Optimized Marketing Placement
- **Prioritize Advertising on Weekends** to directly reach the casual rider segment when they are actively taking their longest and most valuable trips.

---

## Conclusion & Next Steps

This strategy leverages a previously untapped behavioral pattern (ride duration and weekend usage) to create a highly targeted incentive.

- **Next Steps**: Implement a **pilot A/B test** comparing this ride-time-based campaign against existing marketing efforts to validate the conversion rate and profitability.

---

[ **Full Analysis Report**: [Cyclistic-Bike-Share-Case-Study.pdf](./Cyclistic-Bike-Share-Case-Study.pdf) | **Analysis Scripts**: [Cyclistic Bike-Share Case Study.Rmd](./Cyclistic-Bike-Share-Case-Study.Rmd) ]
