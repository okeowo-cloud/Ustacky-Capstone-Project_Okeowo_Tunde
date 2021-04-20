# Nigeria-COVID-19-Data-Analysis-Using-Python
Data Scientist Microdegree Capstone Project

## Project Description:

Coronavirus disease (COVID-19) is an infectious respiratory disease caused by a newly discovered 
coronavirus(SARSCOV2). It affected major countries of the world including Nigeria.

The role of this project is to:

* Analyze the outbreak of the disease in Nigeria using data from the Nigeria
  Centre for Disease Control (NCDC) official [website](https://covid19.ncdc.gov.ng/).

* Analyze the effect of the pandemic on the Nigerian Economy using external dataset such as state budget data, 
  Real Domestic Gross Product data (RealGDP).

* Analyze the effect of the pandemic on Nigeria states revenue using data from the Nigeria Bureau of Statistics
  official [website](https://www.nigerianstat.gov.ng/)

# Steps

This project is completed mainly in three steps which are:

1. Data Collection

2. Data Cleaning and Preprocessing

3. Data Analysis and Visualization

## 1. Data Collection

Data was obtained through four major ways:

a. Nigeria Covid-19 Data Scrapping from the official NCDC [website](https://covid19.ncdc.gov.ng/)

b. Global Covid-19 Data was imported from John Hopkin repository: 

[Global_daily_confirmed_cases](https://github.com/CSSEGISandData/COVID-19/raw/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv)

[Global_daily_recovered_cases](https://github.com/CSSEGISandData/COVID-19/raw/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_recovered_global.csv')

[Global_daily_death_cases](https://github.com/CSSEGISandData/COVID-19/raw/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv)

c. from provided external datasets such as covid_ext, budget_data, RealGDP and covidnig.

d. optional dataset from [Nigeria Bureau of Statistic](https://www.nigerianstat.gov.ng/) for State revenue 
between Q1 and Q2 2020.

## 2. Data Cleaning and Preprocessing

After data was collected, dataframe was viewed using df.head() and df.info() method. 

Necessary cleaning and preprocessing steps carried out include:

a. renaming the State column in dataframe so as to be able to allow merge operation

b. Some states name in state columns were renamed such as Cross river to Cross River; Akwa-Ibom  to Akwa Ibom etc.

c. unwanted columns in global data was deleted such  as Lat, Long, Province/State and Country/Region.

d. comma (,) in numerical data was removed to allow easy arithmetic operation.

e. Nigeria data was extracted from global data and date correctly formatted to datetime.

f. unwanted columns in state revenue were dropped, other column was rename, and the two dataframes were merged


## 3. Data Analysis and Visualization


### TO DO A- Summary of COVID-19 OUTBREAK in Nigeria

I determine from the covid_NCDC scrapped dataframe;

a. The total number of Laboratory confirmed cases
b. The total number of discharged cases
c. The total No. of Cases (on admission) and 
d. The total number of death cases.

Data was Visualized using a bar plot.

The percentage (%) recoveries of Nigerians from covid-19 was estimated

### TO DO B-

I Generated a Bar plot that shows the Top 10 states in terms of Confirmed Covid cases by Laboratory test

### TODO C - 

I Generated a Bar plot that shows the Top 10 states in terms of Discharged Covid cases.

### TODO D-

I Generated a plot that shows the top 10 states in terms of Death cases 

### TODO E-

I Determined the daily infection rate for Nigeria Covi-19 infection and visualized
the data on a line plot

### TODO F - 

I Calculated the maximum infection rate (Number of new cases) and determined the date of occurence


### TODO G-

I Calculated the maximum recovery rate (No recovered per day) and determined the date of occurence

### TODO H -

I Calculated the maximum death rate (No of Deaths per day) and determined the date of occurence

I Generated a line plot for the above

### TODO I -

a. I Determined the relationship between the external dataset and the NCDC COVID-19 data:

   i. relationship between No. of Lab Confirmed Cases and Overall CCVI
   
   ii. relationship between No. of Death cases and Overall CCVI 
   
b. I generated a line plot of top 10 confirmed cases and the overall community vulnerability index on the same axis. 

c. I generated a line plot of top 10 Death cases and the overall community vulnerability index on the same axis

### TODO J - 

I Determined the relationship between the external dataset and the NCDC COVID-19 data:

i. I determined the relationship between No. of Lab confirmed Cases and Population 

ii. I determined the relationship between No. of Lab confirmed Cases and Population Density

### TO DO K-

I determined the relationship between No. Deaths and Population

I determined the relationship between No. Deaths and Population Density


### TODO L - 

I Determined the effect of the Pandemic on the economy by comparing the Real GDP value Pre-COVID-19 with Real GDP in 2020 (COVID-19 Period, especially Q2 2020)


### TO DO M -

I Determined the effect of the Pandemic on states Budget Allocation by determining the relationship between the CCVI data of external data set and budget reduction in top 10 states with greatest and smallest budget reduction.

I also determined the mean CCVI index and budget reduction in top 10 states with greatest and smallest budget reduction.


### TO DO N -

I determined the effect of the pandemic on state revenue for top 10 states with largest revenue and top 10 states with
the least revenue by comparing the Q1 revenue against Q2 revenue

I also determined the percentage change in revenue between Q1 and Q2 in all the states and plot a bar graph to describe the data


# INSIGHTS

* Nigeria experienced very large recovery (about 90%) with very minimal amount of deaths from Covid-19

* Lagos, FCT, plateau, Oyo, Kaduna, Kano were amoung the top 10 states with highest number of Lab confirmed cases
  suggests that population is a key factor to disease spread.

* All except ondo amongst the top 10 states with highest number of Lab confirmed cases also were among the top 10 
  states with the highest number of discharged cases, indicating that most of the confirmed cases recovered from the
  disease.

* Most of the states mentioned above also contributed to the top 10 states with highest death cases, with lagos
  contributing the highest. Delta wasn't among the top 10 states with highest Lab confirmed cases but nevertheless
  made it to the list of top 10 state with highest death. indicating that most covid-19 patient in Delta didn't recover
  from the disease.

* The Nigeria Daily Lab confirmed cases suggest there were two waves of the covid-19 pandemic

* The first wave was lesser and occured during the second quarter of 2020 (between April - june)

* The Second wave was stronger and occured during the first quarter of 2021.

* The Nigeria daily infection rate is approximately 367 Persons per day

* The Maximum number of daily infection is 2464 Persons and occured on the 23rd of January 2021 (during the second wave)

* The Nigeria daily recovery rate is approximately 346 Persons per day

* The maximum number of daily of recovery is 11188 Persons and occured on the 4th of August 2020

* Data also showed that there were two waves of covid-19 deaths corresponding to the waves of the infection

* The Nigeria daily Death rate is approximately 5 Persons per day

* The maximum number of daily death is 31 Persons and occured on the 6th of June 2020 (during the first wave)

* Based on the overall community vulnerability index, the impact of Covid-19 in the 10 highest Lab confirmed states
  was highest in Kaduna and Kano. Lagos, Ondo and Edo are the least vulnerable and received the least impact. 

* Data showed that there is a Linear relationship between the Number of Lab Confirmed cases and Population/Population density

* Nigeria RealGDP value dropped in the second quater (Q2) of 2020 as compared against pre-covid period. This
  implies that Covid-19 had a Negative impact on the Nigerian Economy especially during the second quarter of 2020.

* The Mean Overall Community Vulnerability Index(CCVI) of top 10 states with largest budget reduction (mean=277.071bn) is 0.36

* The Mean Overall Community Vulnerability Index(CCVI) of top 10 states with smallest budget reduction (mean=29.216bn) is 0.57

* Analysis from regression plot shows that a linear relationship exist between budget reduction and CCVI.

* States with low CCVI (pandemic impact) had the greatest reduction in budget

* States with high CCVI (pandemic impact) had the least reduction in budget

* Lagos state had the highest drop in revenue during Q2 among the 10 states with high income

* All other states except Kano with high revenue had a drop in revenue during the second quarter

* Among the low revenue states, Gombe, Sokoto and Katsina had an increase in revenue during the second quarter

* Among the low revenue states, Ekiti, Jigawa and Taraba had a drop in revenue at Q2 while Kebbi and Yobe had little
  or No change in revenue
  
* Gombe had the highest increase in revenue estimated at about 143% while Osun had the highest drop in revenue estimated at about -72%

* A large no. of states  experienced a loss in revenue during the second quarter of 2020.



# Future Works

Future work would be to answer more questions of the 
Covid-19 pandemic in Nigeria such as :

(a.) Is there a relationship between age and susceptibility to the infection?

What is the age with the max. frequency of infection?
What is the age with the min. frequency of infection?

(b.) Is there a relationship between age and recovery from infection?

What are the ages with the max. frequency of recovery?
What are the ages with the min. frequency of recovery?

(c.) Is there a relationship between age and death from the infection?

What are the ages with the max. frequency of discharge?
What are the ages with the min. frequency of discharge?



# Standout Section

The major standouts in this project are:  

a. The relationship carried out between buget reduction and overall CCVI

b. The analysis carried out on Nigeria state revenue before covid (Q1) and during covid (Q2) in all the states.










