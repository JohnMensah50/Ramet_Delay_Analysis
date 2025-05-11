# Ramet_Delay_Analysis
This is the R code used for the analysis of "Delayed effects of water-limiting conditions influence the ramet demography of a native iterocarpic thistle"

*Data*

**Raw unprocessed Transtion Data from the Field**
1. "UAASOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot A in Arapaho
2. "UABSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot B in Arapaho
3. "UACSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot C in Arapaho
4. "UADSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot D in Arapaho
5. "UNMSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot M in Niobrara
6. "UNKSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot K in Niobrara
7. "UNLSOverview19902009RAMET 20230630.xlsx" = Original Transition data for Plot L in Niobrara

**Analysis Ready-Data for Vital Rate Estimation**
1. UAA_single.csv: Processed and cleaned data from "UAASOverview19902009RAMET 20230630.xlsx"
2. UAB_single.csv: Processed and cleaned data from "UABSOverview19902009RAMET 20230630.xlsx"
3. UAC_single.csv: Processed and cleaned data from "UACSOverview19902009RAMET 20230630.xlsx"
4. UAD_single.csv: Processed and cleaned data from "UADSOverview19902009RAMET 20230630.xlsx"
5. UNM_single.csv: Processed and cleaned data from "UNMSOverview19902009RAMET 20230630.xlsx"
6. UNK_single.csv: Processed and cleaned data from "UNKSOverview19902009RAMET 20230630.xlsx"
7. UNL_single.csv: Processed and cleaned data from "UNLSOverview19902009RAMET 20230630.xlsx"

**Description of Analysis Ready-Data columns used to handle the field data in the statistical analyses**

Column name	Description
Species:	WL = wavyleaf thistle (Cirsium undulatum)
SITE:	Study site; APP = Arapaho Prairie Preserve; NVP = Niobrara Valley Preserve
PLOT:	Plot Number: A, B, C, D
Year:	Current year of survey data (t)
Month:	Month of survey data
Ramet:	Unique identification number (aluminum tag) for the ramet
stage.modified:	Current stage of the ramet
PrevStage:	Previous state of the ramet, for the immediate past year (t - 1) of ramet
PrevYear:	Previous year of survey data (t – 1)
NextYear:	Next year of survey data (t + 1)
NextStage:	Next stage observed (fate) of ramet (stage at t + 1), given state of ramet in current year, t
firstYear:	First year the ramet appeared (for the first time)
firstStage:	Stage of the ramet when it was first observed 
lastYear:	Last year the ramet was seen
lastStage:	State of the ramet when last observed
Survival:	Fate of the ramet in the next year: alive = Yes or not alive = No; denotes the fate / state of the ramet (alive/not alive) in year t+1; does not mean the ramet was alive/not alive in  t, but rather whether ramet was alive/not alive in year t+1.

**Descriptions of life stages as described in the data and used for statistical analysis**
SR:	Single Rosette
SF:	Flowering Single Rosette
MR:	Multiple Rosette
MF:	Flowering Multiple Rosette
Seedling:	Seedling rosette, with cotyledons 
Not tagged:	Ramet measured but not given unique numerical tag (in 2007 – 2009); these data were used only in recruitment analyses 
First Appearance:	Indicated no previous stage recorded; useful for identifying new sprout recruits
Inactive:	Ramets that was vegetatively active, then missing for 1 – 2 years or 3 observation periods before re-emerging at a tag.


**Estimated Vital rates**
1. "VR_Arapahoe.csv" = estimated vital rates for all ramets demographic stages at Arapaho
2. "VR_Arapahoe.csv" = estimated vital rates for all ramets demographic stages of at Niobrara

**Asymptotic Population Growth Rates estimated from Matrix Population Models**
1. Lambda_Arapahoe.csv = Estimated Population Growth Rates for Arapaho
2. Lambda_Niobrara.csv = Estimated Population Growth Rates for Niobrara

**Weather Data**
Weather data (Monthly mean temperature and Monthly total rainfall) was downloaded from Prism Climate Group website (https://prism.oregonstate.edu/explorer/) 
using the GPS coordinates of the study sites
1. Arapaho.Weather.csv
2. Niobrara.Weather.csv

*R codes*
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

