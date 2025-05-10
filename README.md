# Ramet_Delay_Analysis
This is the R code used for the analysis of "Delayed effects of water-limiting conditions influence the ramet demography of a native iterocarpic thistle"

** Data ***

##Raw unprocessed Transtion Data from the Field##
1. "UAASOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot A in Arapaho
2. "UABSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot B in Arapaho
3. "UACSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot C in Arapaho
4. "UADSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot D in Arapaho
5. "UNMSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot M in Niobrara
6. "UNKSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot K in Niobrara
7. "UNLSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot L in Niobrara

##Analysis Ready-Data for Vital Rate Estimation##
1. UAA_single.csv: Processed and cleaned data from "UAASOverview19902009RAMET 20230630.xlsx"
2. UAB_single.csv: Processed and cleaned data from "UABSOverview19902009RAMET 20230630.xlsx"
3. UAC_single.csv: Processed and cleaned data from "UACSOverview19902009RAMET 20230630.xlsx"
4. UAD_single.csv: Processed and cleaned data from "UADSOverview19902009RAMET 20230630.xlsx"
5. UNM_single.csv: Processed and cleaned data from "UNMSOverview19902009RAMET 20230630.xlsx"
6. UNK_single.csv: Processed and cleaned data from "UNKSOverview19902009RAMET 20230630.xlsx"
7. UNL_single.csv: Processed and cleaned data from "UNLSOverview19902009RAMET 20230630.xlsx"

### Estimated Vital rates ######
1. "VR_Arapahoe.csv" = estimated vital rates for all ramets demographic stages at Arapaho
2. "VR_Arapahoe.csv" = estimated vital rates for all ramets demographic stages of at Niobrara

###Asymptotic Population Growth Rates estimated from Matrix Population Models
1. Lambda_Arapahoe.csv = Estimated Population Growth Rates for Arapaho
2. Lambda_Niobrara.csv = Estimated Population Growth Rates for Niobrara

###### Weather Data
Weather data (Monthly mean temperature and Monthly total rainfall) was downloaded from Prism Climate Group website (https://prism.oregonstate.edu/explorer/) 
using the GPS coordinates of the study sites
1. Arapaho.Weather.csv
2. Niobrara.Weather.csv

### R codes#####
1. "UAA.qmd", "UAB.qmd", "UAC.qmd", "UAD.qmd", "UNM.qmd", "UNL.qmd", "UNK.qmd" are r codes that were used to clean and 
process the raw field transition data to analysis-ready data format.
2. Exploratory analysis.qmd = R code used to generate patterns in the stage-specific abundance over times
3. Weather Analysis.qmd = R code for analysing weather data, including calculating for Standardized Precipitation Evapotranspiration Index (SPEI)
4. "VR_Arapahoe.qmd" and "VR_Niobrara.qmd" = R codes used for estimating vital rates and asymptotic population growth rate for Arapaho and Niobrara
5. Lag.select.qmd = R code used to explore the optimum time-lag for delayed effect analysis
6. FLM - stage transition.qmd = R code for analysing delayed effect of weather variables on ramet demography using Functional Linear Models
7. make_data.R = R code for creating lag variables of weather appropriate for Functional Linear Model analysis for delayed effect. 
The make_data.R code was modified from the code originally produced by Dr. Drew Tyre in Tenhumberg et al. (2018)
8. Simulation Analysis.qmd: R code used for the Population Viablilty Analysis

