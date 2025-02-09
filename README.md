# Oil_Well_Profibility_Analysis_S9

# Project Overview
OilyGiant, a mining company, aims to identify the most profitable location for a new oil well. The objective is to build a predictive model that estimates oil reserves in potential wells and selects the region with the highest profit margin. The analysis includes risk assessment using the Bootstrapping technique.

# Project Workflow
1. ***Data Preparation***
  - Load and clean geological exploration data from three regions.
  - Understand the dataset structure and describe preprocessing steps.
2. ***Model Training and Evaluation***
  - Split the data into training and validation sets (75:25).
  - Train a Linear Regression model for each region.
  - Predict oil reserves in the validation set and evaluate model performance using RMSE.
  - Store predictions and actual values for further analysis.
3. ***Profit Calculation Preparation***
  - Define key values for financial calculations.
  - Determine the minimum volume of reserves required for a well to break even.
  - Compare this value with the average predicted reserves in each region.
4. ***Profit Calculation***
  - Select the top 200 wells with the highest predicted reserves.
  - Calculate the total predicted volume of reserves for the selected wells.
  - Compute the expected profit based on oil prices and development costs.
  - Identify the most profitable region and justify the choice.
5. ***Risk Analysis Using Bootstrapping***
  - Use the Bootstrapping technique with 1000 samples to simulate profit distributions.
  - Calculate the average profit, 95% confidence interval, and probability of losses for each region.
  - Select the region with the highest average profit while ensuring the risk of loss remains below 2.5%.

# Dataset Description
Geological exploration data for three regions are provided in the following files:

  ***geo_data_0.csv***
  
  ***geo_data_1.csv***
  
  ***geo_data_2.csv***

# Features:
  ***id*** – Unique identifier for an oil well.
  
  ***f0, f1, f2*** – Geographical features of the well (specific meaning undisclosed).
  
  ***product*** – Volume of oil reserves in the well (in thousand barrels).

# Project Constraints & Assumptions
- ***Linear regression*** is the only suitable model for predictions.
- Each region is initially explored with ***500 points***, from which the ***top 200 wells*** are selected for final profit calculations.
- The total development budget is ***$100 million*** for 200 wells.
- Each barrel of oil generates ***$4.5 in revenue***, meaning one unit in the dataset (thousand barrels) corresponds to $4,500 in revenue.
- Only regions with a loss ***risk below 2.5%*** will be considered. The region with the highest expected profit among them will be selected.
- The dataset is ***synthetic***, and real-world contract details and well characteristics are not disclosed.

# Final Deliverables
- A well-trained predictive model for oil reserves estimation.
- A clear recommendation for the most profitable region.
- A risk assessment report justifying the selection.
