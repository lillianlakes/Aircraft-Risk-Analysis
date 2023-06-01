# Aircraft Risk Analysis

## Overview

## Business Understanding
Our stakeholders are exploring the airplane industry, both commercial and private, and want to assess the risk before making any decisions. 
The Federal Aviation Administration defines risk as "the probability and possible severity of accident or loss from exposure to various hazards, including injury to people and loss of resources." We explored the data through this lens and with the goal of answering these main questions: 
  1. How can we most accurately quantify risk in aviation using data from past accidents? 
  2. Which sector is more risky: commercial or private? 
  3. Which particular aircraft models can we recommend to our stakeholders? 

## Data Understanding and Analysis
### Data Exploration
We used the [NTSB aviation accident](https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses) database from Kaggle for our analysis. 
The database contains reports of civil aviation accidents that occured in the United States, U.S. Territories, or international waters, from 1962 to 2022. The information included the following main categories:
  1. Where and when the accident occured, often by state or latitude and longitude
  2. Details of the specific aircraft, included make and model
  3. External factors, such as weather or airport when relevant
  4. Results of the incident, including the severity of harm to passengers and damage to the aircraft.

The original dataset provides us with a number of limitations. First, we only have information on accidents that occured, and no information about total flights taken each year. This made it impossible to determine the frequency at which incidents occured, so we were left to only examine the "severity of accident" parameter of risk. Furthermore, the methods of reporting appeared to change significantly throughout time, causing many inconsistencies and null values in the dataset. 

After filtering the dataset to include only airplane-specific reports, our next largest filter was by date. After plotting the number of airplane incidents in a graph, we noticed a levelling off around 2009. After doing some external research, we discovered that 2009 was the last year the U.S. experienced a large fatal commercial accident, which prompted the FAA to implement new pilot regulations. Since our goal is to compare airplane models, we decided to only use data points after 2009 in order to have consistency in pilot safety protocols.   

### Data Analysis


## Conclusion
