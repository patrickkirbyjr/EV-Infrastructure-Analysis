# EV Infrastructure Analysis

## Summary
This project analyzes the distribution of electric vehicle (EV) charging stations across the United States to identify which states are most in need of additional charging infrastructure. Publicly available datasets on EV stations, EV registrations, state populations, gas stations, and state areas were used in conjunction with machine learning methods to predict whether states are considered relatively underbuilt or relatively overbuilt. Location data from all EV stations across the continental US were used to visualize coverage within specific radii for select states. 

## Project Goals
1. Acquire, clean, and visualize data on the current US electric vehicle charging infrastructure (Part 1)
2. Use machine learning to identify the states that are most underbuilt and overbuilt in terms of EV charging infrastructure (Part 2)
3. Conduct geospatial analysis to determine the coverage area for underbuilt states (Part 3)

## Data Sources

EV Station Data: https://afdc.energy.gov/data_download

EV Registration Data: https://afdc.energy.gov/data/10962

State Population Data: https://www.census.gov/data/tables/time-series/demo/popest/2020s-state-total.html

Gas Station Data: https://afdc.energy.gov/files/u/data/data_source/10333/10333_gasoline_stations_year.xlsx

State Area Data: https://www.census.gov/geographies/reference-files/2010/geo/state-area.html

## Findings
1. California has, by far, the most EV stations with 17,797 in total.
2. EV coverage is denser along the coasts and quite sparse across the Midwest.
3. New Jersey and Nevada have the highest ratio of EVs to available charging stations.
4. Louisiana and Mississippi have the highest ratio of people to available charging stations.
5. California has, by far, the most EV station saturation by population.
6. Linear models proved to be the most statistically effective in predicting underbuilt states compared to random forest and gradient boosting methods.
7. Strong predictors of EV infrastructure include the number of EV registrations and population.
8. Weak predictors of EV infrastructure include the number of gas stations and state areas (although state areas can be included to reduce extremes).
9. Models consider Texas, Florida, New Jersey, and Illinois to be the most underbuilt states in terms of EV charging station infrastructure.
10. Pennsylvania, which models consider to be slightly underbuilt compared to the rest of the country, has widespread EV station coverage in the east and west but lacks coverage in the more rural mid-state areas.

## Coverage Maps
Coverage maps were generated for the states identified by the linear model as the most underbuilt in terms of EV infrastructure. My home state of Pennsylvania was also mapped. Using a custom R function, EV stations in each state were buffered by distances of 5, 10, 15, and 20 miles to visualize the areas in close proximity to an EV charging station. These different buffer zones represented various conveniences from a few minutes away (5 miles) to slightly inconvenient (20 miles).

## Next Steps
- Add additional factors to geospatial analysis (population, EV ownership, highways, etc.)
- Analyze and compare US states to Norway (world leader in EV infrastructure)