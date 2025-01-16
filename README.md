## Overview:
Given a dataset which contains 4 different temperature sensors data for each part id, we need to find whether the producing metal part is good or not based on the temperature captured.    

Actions:
    1. EDA
    2. Preprocessing and Feature Engineering
    3. Model Building
    4. Evaluation

### Insights from EDA
1. The temperature captured for each part id is in sequal manner. For Example, if machine producing one part then 4 different sensors are oberving the temperature for then next ~5 mins, then the production of the next part id starts
2. From the chart, Green and Red having the highest temperature across all part id 
3. The time and 4 temperatures dont have any relation. Timestamp is just a time of capture the temperature. 
4. This is example of imbalance data because 93% (276/295) belong to 0 label. This gives clue where we should use PR Curve for performance analysis. Tree based Algorithm perform well on imbalance dataset like XGBoost, so we will use it.

## Summary
1. We have created only some statistical features, but we can increase the complexity of the model by incorporating more 
features like COV, median, addition/substractions of 4 temperations, ranges (min-max), scale/ratios etc.  
2. A simple naive or baseline model can be used to know the baseline accuracy before moving to the more complex model
