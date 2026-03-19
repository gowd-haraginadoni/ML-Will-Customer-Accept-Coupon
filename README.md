# Will the Customer Accept the Coupon?

## Overview
This project analyzes driver behavior and coupon acceptance patterns using data from a UCI Machine Learning repository survey conducted via Amazon Mechanical Turk. The goal is to identify key factors that influence whether drivers accept coupons delivered to their mobile devices while driving.

## Dataset
- **Source**: UCI Machine Learning Repository
- **Size**: 12,079 observations (after cleaning)
- **Coupon Types**: Bar, Coffee House, Carry Out & Take Away, Restaurant (<$20), Restaurant ($20-$50)
- **Overall Acceptance Rate**: 56.93%

## Key Findings

### Bar Coupon Analysis

**Frequency of Bar Visits is the Strongest Predictor**
- Drivers who visit bars **>3 times/month**: 76.17% acceptance
- Drivers who visit bars **≤3 times/month**: 37.27% acceptance
- Frequent bar-goers are more than twice as likely to accept bar coupons

**Demographic Patterns**
- **Age + Frequency**: Drivers over 25 who visit bars >1/month show 68.98% acceptance vs. 33.77% for others
- **Social Context**: Drivers with no kids as passengers and non-farming occupations show 70.94% acceptance
- **Young Frequent Visitors**: Drivers under 30 who visit bars >1/month show 71.95% acceptance

**Key Profile of Bar Coupon Acceptors**
- Regular bar-goers (>1 visit/month)
- Younger adults (under 30) or at least over 25
- Traveling without children
- Not working in farming-related occupations

### Weather Impact on Coupon Acceptance

**Carry-Out Coupons**: Weather-resistant with highest acceptance (61-77%)
- Peak in snowy weather (31.5% of total acceptance) when convenience is prioritized
- Consistently high across all conditions

**Restaurant Coupons**: Highly weather-dependent
- Cheap restaurants (<$20): 26.1% acceptance in sunny weather vs. 17.4% in rainy
- Expensive restaurants ($20-50): Drop to 31% in snowy conditions

**Coffee House Coupons**: Weather-independent
- Maintain stable 17-23% acceptance across all weather conditions
- Acceptance increases with temperature (52% at 80°F vs. 45% at 30°F)
- Driven by demand for iced coffee and air-conditioned spaces in warm weather

**Bar Coupons**: Lowest acceptance (13-16%) regardless of weather

### Passenger Type Impact

**Friends as Passengers**: Highest acceptance rates
- Cheap restaurants: 80.35%
- Carry-out: 75.95%

**Kids as Passengers**: Suppress acceptance for adult venues
- Bar coupons: 20.62% (vs. 56-73% without kids)
- Expensive restaurants: 36.88%

**Partners**: Moderate acceptance, especially for mid-range restaurants (62.50%)

**Alone**: Variable acceptance depending on coupon type

### Time of Day Patterns

**Carry-Out Coupons**: Consistently high acceptance at all times
- Demonstrate appeal as convenient dining option regardless of hour

**Bar Coupons**: Strong time-dependent patterns
- Peak acceptance at 10 PM (nightlife hours)
- Lowest acceptance at 2 PM (work hours)
- Reflects social appropriateness of bar visits at different times

## Conclusions

1. **Behavioral Habits Trump Demographics**: The strongest predictor of bar coupon acceptance is existing bar-going frequency, not age or income alone.

2. **Context Matters**: Social context (passengers, time of day, weather) significantly influences acceptance for experience-based venues (bars, restaurants) but has minimal impact on convenience-focused options (carry-out).

3. **Weather Resistance by Category**:
   - Convenience coupons (carry-out) thrive in all weather
   - Experience coupons (sit-down dining, bars) require pleasant conditions

4. **Strategic Targeting**: Coupon campaigns should target:
   - Bar coupons: Frequent bar-goers, evening hours, drivers without kids
   - Expensive Restaurant coupons: Sunny weather, social passengers (friends/partners)
   - Cheap Restaurant coupons: Sunny weather, drivers with kids
   - Coffee coupons: Any weather, focus on warm temperatures for iced beverages
   - Carry-out: Universal appeal, especially effective in adverse weather

## Technologies Used
- Python 3.14.3
- pandas
- matplotlib
- seaborn
- numpy
- Jupyter Notebook

## Files
- `prompt.ipynb`: Main analysis notebook
- `data/coupons.csv`: Dataset
- `images/`: Visualizations generated from analysis

## Repository
- [GitHub Repository](https://github.com/gowd-haraginadoni/ML-Will-Customer-Accept-Coupon)
- [Jupyter Notebook](https://github.com/gowd-haraginadoni/ML-Will-Customer-Accept-Coupon/blob/main/prompt.ipynb)
