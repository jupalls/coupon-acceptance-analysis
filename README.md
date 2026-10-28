# Will the Customer Accept the Coupon?

An exploratory analysis of when drivers accept coupons delivered to their phones, using survey data from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation).

**Notebook:** [coupon_acceptance_analysis.ipynb](coupon_acceptance_analysis.ipynb)

## The question
Drivers were shown a driving scenario (destination, time of day, weather, passengers) and a coupon for a nearby business, then asked whether they would use it. Five different coupon types were offered namely: carry out, cheap restaurants (under \$20), coffee houses, bars, and expensive restaurants (\$20–50). The goal is to understand who accepts the coupons.

## Data based on the file
- 12,684 survey responses (12,610 after removing duplicates), each labelled accepted or rejected.
- Driver details: age, income, occupation, and how often they visit bars, coffee houses and restaurants.
- Situation details: destination, passengers, weather, time of day, distance to the business, and coupon expiry.

## Key findings
- Overall, 57% of coupons were accepted and the rate depends heavily on coupon type.
- Carry out (73%) and cheap restaurants (71%) are accepted far more often than bars (41%) or expensive restaurants (44%).
- Regular bar-goers (more than 3 times a month) accept 77% of bar coupons, against 37% for everyone else. Being under 30, or having no children in the car, also points to acceptance.
- Coffee house regulars (1+ visits a month) accept 66%, and acceptance is highest when the offer arrives at 10AM (64%). Drivers who don't visit coffee houses accept only 19%.

## Recommendations
1. **Target coupons to people based on their habits.** Send bar and coffee coupons to people who already visit those places; past behaviour is the strongest predictor of acceptance.
2. **Timing matters.** Send coffee coupons in the mid-morning and early afternoon, and avoid drivers on their way home.
3. **Lead with low-cost coupons** (carry out, cheap restaurants) for broad campaigns. 

## Repository contents
- `coupon_acceptance_analysis.ipynb`: the full analysis, with code, charts and findings
- `data/coupons.csv`: the survey dataset

## Next Steps
- Analyse remaining coupon types same way
- Check if there are any other cross dependency overlaps 
