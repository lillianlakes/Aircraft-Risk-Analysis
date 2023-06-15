# Aircraft Risk Analysis
Authors: Lillian Lakes, Madeleine Smithers, and Rajesh Reddy

To explore our findings further, please visit our [Tableau Dashboard](https://public.tableau.com/app/profile/rajesh.reddy5034/viz/ProjectPhase1Dashboard/Dashboard1#1), our [Live Project Presentation](https://youtu.be/TvrjEL8AaEg) and our [Project Deck](https://docs.google.com/presentation/d/1AkNtNh1cPJnr5ddkoAes-2Pz2WXlAYeAHy00Agh9kxg/edit#slide=id.g24d4fbc3b08_0_2278). 

## Business Understanding
Our stakeholders are exploring the airplane industry, both commercial and private, and want to assess the risk before making any decisions. 
The Federal Aviation Administration defines risk as "the probability and possible severity of accident or loss from exposure to various hazards, including injury to people and loss of resources." We explored the data through this lens and with the goal of answering three main questions: 
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
After cleaning our data, we decided to explore relationships between accident severity and attributes of the airplanes, including whether commercial or private, the make, and the model. First, we looked at whether commercial or private airplane accidents resulted in more fatalities. 

<img width="850" alt="Screenshot 2023-06-01 at 6 26 30 PM" src="https://github.com/MaddieSmithers/Aircraft-Risk-Analysis/assets/132934793/52fb3183-3d59-4591-9619-91d829c4646d">

To accurately assess the severity of each accident, we used a metric of 'fatality rate.' To get this number, we looked at the percentage of passengers killed in each accident to account for varying total passengers. We then graphed the average rate over each year since 2010 to identify any trends. 

<img width="850" alt="Screenshot 2023-06-01 at 6 29 33 PM" src="https://github.com/MaddieSmithers/Aircraft-Risk-Analysis/assets/132934793/0cb63ae2-b529-478c-9738-f3860a25e2d9">
<img width="850" alt="Screenshot 2023-06-01 at 6 33 58 PM" src="https://github.com/MaddieSmithers/Aircraft-Risk-Analysis/assets/132934793/178ccb29-f841-48e3-a8db-5a58f87d8397">

Our data clearly shows that the average fatality rates are significantly higher in private airplanes, leading us to the conclusion that passengers are overall 75% safer in commercial planes than in private planes. 

Next, we grouped our data by make and model to identify which planes would carry the least amount of risk for our stakeholders. We only considered models still in production today to ensure our conclusions would be relevant to potential buyers. 

<img width="850" alt="Screenshot 2023-06-01 at 6 36 47 PM" src="https://github.com/MaddieSmithers/Aircraft-Risk-Analysis/assets/132934793/ffb6be6f-1604-4034-b773-92ef3dde58bd">

<img width="850" alt="Screenshot 2023-06-01 at 6 39 28 PM" src="https://github.com/MaddieSmithers/Aircraft-Risk-Analysis/assets/132934793/2d89cb16-bd39-43a8-a596-2d6a41ee142d">


## Conclusion

We arrived at three main recommendations for our clients based on a combination of business understanding and data analysis: 

 1. On average, accidents involving commercial airplanes result in lower fatality rates than those involving private airplanes. Because of this, we reccomend our stakeholders to venture either soley or predominantly into the commercial aviation sector in order to minimize risk. 
 2. Of the top commercial airline manufacturers, Boeing has consistently showed the lowest fatality rates and is the manufacturer we would recommend. Of the models currently in production, the Boeing 737 and the Boeing 777 have the lowest average fatality rates and would be most effective in minimizing accident severity. 
 3. Of the top private airline manufacturers, Cessna shows the lowest average fatality rate and is therefore the manufacturer we would recommend to our client for the private sector. Of models currently in production, the 172 and 182 have the lowest fatality rates. As an alternative, we would also recommend the Cirrus SR20 or SR22 as they have also shown significantly lower fatality rates over our years charted.

## Repository Contents

    .
    ├── data                    # Original CSVs and cleaned master data CSV
    ├── working notebooks       # ipynb files from all team members
    ├── .gitignore              # files to ignore
    ├── Airline Risk Analysis   # PDF version of presentation slides
    ├── Final Notebook          # Final narrative notebook of data analysis 
    └── README.md
