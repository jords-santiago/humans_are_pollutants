# Humans Are The Pollutants
An Analysis of World Development Indicators towards adverse impact to our Environment

## TLDR

* China, United States, Russia, India and Japan were chosen for analysis as they rank among the top in gas emissions.
* In general, world development indicators such as GDP and population growth increase along with gas emissions and air pollution but this is expected as the countries sampled are those fairly developed.
* To see a significant trend along with GDP and population, more data should be acquired as data from 2010 to 2017 were available.
* Forest Area is seen to have negative correlation with gas emission and pollution both on taking all 5 countries and for each country in general.
* It is recommended to look further in to forest/tree/vegetation data with respect to gas emissions and air pollution as it seems to contribute against them.

## Introduction

### Background

The statement "humans are Earth's top pollutants" has been thrown here and there.  Unfortunately, this is very much true.  All of the factors contributing to the adverse effects in our environment can be very much traced back to some technology that we developed over time to make our lives easier.  Other than making a return to living like in pre-historic times, an equilibrium needs to be reached where we continue to advance our quality of life while ensuring Earth can hold up.

### Business Task

In search of that equilibrium, this analysis will use public data from the World Bank Databank to determine any relation to some World Development Indicators against Environment issue indicators (e.g. CO2 emissions, GHG emissions, air pollution).  After going over through these indicators,  observations and insights may be acquired to be acted upon to save Earth while we live our lives better.

### Objectives

* Identify some top countries that largely contribute to gas emissions and air pollution for further analysis on their World Development Indicators.
* Identify general trends of gas emissions and air pollution with the acquired World Development Indicators.
* Suggest some indicators that may contribute against gas emissions and air pollution to be looked further into.

## Methodology

### Data Source

All of the data were acquired in the World Development Indicators of the World Bank Open Data site.  From its [World Development Indicators DataBank](https://databank.worldbank.org/source/world-development-indicators#), multiple groups were queried and extracted separately for convenience. 

[CO2 Emissions:](https://github.com/jords-santiago/humans_are_pollutants/blob/main/01_DataSources/01_Raw/original_zip/World_Bank_CO2_World_Development_Indicators.zip)

|Series Code | Series Name |
| --- | --- |
|EN.ATM.CO2E.GF.ZS | CO2 emissions from gaseous fuel consumption (% of total) |
|EN.ATM.CO2E.KT | CO2 emissions (kt) |
|EN.ATM.CO2E.LF.ZS | CO2 emissions from liquid fuel consumption (% of total) |
|EN.ATM.CO2E.PC | CO2 emissions (metric tons per capita) |
|EN.ATM.CO2E.SF.ZS |CO2 emissions from solid fuel consumption (% of total) |
|EN.CO2.BLDG.ZS | CO2 emissions from residential buildings and commercial and public services (% of total fuel combustion) |
|EN.CO2.ETOT.ZS | CO2 emissions from electricity and heat production, total (% of total fuel combustion) |
|EN.CO2.MANF.ZS | CO2 emissions from manufacturing industries and construction (% of total fuel combustion) |
|EN.CO2.OTHX.ZS | CO2 emissions from other sectors, excluding residential buildings and commercial and public services (% of total fuel combustion) |
|EN.CO2.TRAN.ZS | CO2 emissions from transport (% of total fuel combustion) |

[Other Gas Emissions:](https://github.com/jords-santiago/humans_are_pollutants/blob/main/01_DataSources/01_Raw/original_zip/World_Bank_Othergas_World_Development_Indicators.zip)

| Series Code | Series Name |
| --- | --- |
| EN.ATM.GHGO.KT.CE | Other greenhouse gas emissions, HFC, PFC and SF6 (thousand metric tons of CO2 equivalent) |
| EN.ATM.GHGT.KT.CE | Total greenhouse gas emissions (kt of CO2 equivalent) |
| EN.ATM.HFCG.KT.CE | HFC gas emissions (thousand metric tons of CO2 equivalent) |
| EN.ATM.METH.KT.CE |Methane emissions (kt of CO2 equivalent) |
| EN.ATM.NOXE.KT.CE | Nitrous oxide emissions (thousand metric tons of CO2 equivalent) |
| EN.ATM.SF6G.KT.CE | SF6 gas emissions (thousand metric tons of CO2 equivalent) |

[Air Pollution:](https://github.com/jords-santiago/humans_are_pollutants/blob/main/01_DataSources/01_Raw/original_zip/World_Bank_Pollution_World_Development_Indicators.zip)

| Series Code | Series Name |
| --- | --- |
| EN.ATM.PM25.MC.M3 | PM2.5 air pollution, mean annual exposure (micrograms per cubic meter) |
| EN.ATM.PM25.MC.T1.ZS | PM2.5 pollution, population exposed to levels exceeding WHO Interim Target-1 value (% of total) |
| EN.ATM.PM25.MC.T2.ZS | PM2.5 pollution, population exposed to levels exceeding WHO Interim Target-2 value (% of total) |
| EN.ATM.PM25.MC.T3.ZS | PM2.5 pollution, population exposed to levels exceeding WHO Interim Target-3 value (% of total) |
| EN.ATM.PM25.MC.ZS | PM2.5 air pollution, population exposed to levels exceeding WHO guideline value (% of total) |

[GDP:](https://github.com/jords-santiago/humans_are_pollutants/blob/main/01_DataSources/01_Raw/original_zip/World_Bank_GDP_World_Development_Indicators.zip)

| Series Code | Series Name |
| --- | --- |
| NY.GDP.MKTP.CD | GDP (current US$) |
| NY.GDP.MKTP.KD.ZG | GDP growth (annual %) |
| NY.GDP.PCAP.CD | GDP per capita (current US$) |
| NY.GDP.PCAP.KD.ZG | GDP per capita growth (annual %) |

[Land Use:](https://github.com/jords-santiago/humans_are_pollutants/blob/main/01_DataSources/01_Raw/original_zip/World_Bank_LandUse_World_Development_Indicators.zip)

| Series Code | Series Name |
| --- | --- |
| AG.LND.AGRI.K2 | Agricultural land (sq. km) |
| AG.LND.AGRI.ZS | Agricultural land (% of land area) |
| AG.LND.FRST.K2 | Forest area (sq. km) |
| AG.LND.FRST.ZS | Forest area (% of land area) |
| AG.LND.TOTL.K2 | Land area (sq. km) |
| AG.LND.TOTL.RU.K2 | Rural land area (sq. km) |
| AG.LND.TOTL.UR.K2 | Urban land area (sq. km) |

[Urbanization/Population:](https://github.com/jords-santiago/humans_are_pollutants/blob/main/01_DataSources/01_Raw/original_zip/World_Bank_Urbanization_World_Development_Indicators.zip)

| Series Code | Series Name |
| --- | --- |
| SP.POP.GROW | Population growth (annual %) |
| SP.POP.TOTL | Population, total |
| SP.RUR.TOTL | Rural population |
| SP.RUR.TOTL.ZG | Rural population growth (annual %) |
| SP.RUR.TOTL.ZS | Rural population (% of total population) |
| SP.URB.GROW | Urban population growth (annual %) |
| SP.URB.TOTL | Urban population |
| SP.URB.TOTL.IN.ZS | Urban population (% of total population) |

Data was gathered for 217 countries and from the last 15 years (2007-2021).

### Exploratory Data Analysis/Preparation/Cleaning

Preparation, Cleaning, Visualization were all done in Jupyter Notebook.  A separate notebook was created to contain all helper functions that will prepare/clean/transform/visualize the data frames.

After cleaning, based on viewing the null values for each dataset, only data from 2010 to 2017 as this the time period that all datasets have in common (no null).  Imputing values with either the mean or median may not be a good approximation as these are country data.

Taking the CO2 emissions, it was determined to further analyze data for these countries:
* United States
* China
* India
* Russia
* Japan

These countries are large in terms of land area and population to have significant impact to the environment for us to look into further.

To normalize the data to possibly mitigate the effect of land area, feature engineering was done where gas emissions data were transformed to be emissions per land area of each country.  Also, the annual change in forest area was calculated.

In summary, after checking the data, the following were observed:
* CO2, Green House Gas (GHG), Methane and Nitrous Oxide emissions data are very much similar to each other with China and the United States are in the top 2 where China is mostly trending upwards on emissions.
* China and India are already at 100% on population exposed to pollution levels.  However, the mean annual exposure, in the given countries, is slightly decreasing/level.  Clearly, United States and Japan have severely reduced the amount of their population subjected to significant air pollution.
* In GDP/GDP per capita, aside from Russia and Japan which have up and downs, GDP is trending upwards.
* In Forest Area data, when the annual change graph was derived, it showed that all 5 countries don't have much change in their forest area but are trending upwards in general.
* For Population/Urbanization, population growth is increasing in general.  However, population growth is slowing down with Japan shows increase in rural population and decrease in urban population.
* After gas emissions data were normalized against respective land areas, it now shows Japan being top in emission per their land area with China coming up next.

## Analysis and Results

For analysis, the following were used:

Gas Emissions/Pollution Indicators

| Dataset | Series Code | Series Description/Name |
| --- | --- | --- |
|CO2| EN.ATM.CO2E.KT.AREA | CO2 emissions per land area (kt/sq. km)|
|Other Gas | EN.ATM.GHGT.KT.CE.AREA | Total greenhouse gas emissions per land area (kt/sq. km of CO2 equivalent) |
|Other Gas | EN.ATM.METH.KT.CE.AREA | Methane emissions per land area (kt/sq. km of CO2 equivalent)|
|Other Gas | EN.ATM.NOXE.KT.CE.AREA | Nitrous oxide emissions per land area (thousand metric tons/sq. km of CO2 equivalent)|
|Pollution | EN.ATM.PM25.MC.M3 | PM2.5 air pollution, mean annual exposure (micrograms per cubic meter)|
|Pollution | EN.ATM.PM25.MC.ZS | PM2.5 air pollution, population exposed to levels exceeding WHO guideline value (% of total) |

World Development Indicators

| Dataset | Series Code | Series Description/Name |
| --- | --- | --- |
| GDP | NY.GDP.MKTP.KD.ZG | GDP growth (annual %) |
| GDP | NY.GDP.PCAP.CD | GDP per capita (current US$) |
| Land Use | AG.LND.FRST.ZS | Forest area (% of land area) |
| Land Use | AG.LND.FRST.K2.CHG | Forest area annual change |
| Urbanization | SP.POP.GROW | Population growth (annual %) |
| Urbanization | SP.RUR.TOTL.ZG | Rural population growth (annual %) |
| Urbanization | SP.URB.GROW | Urban population growth (annual %) |

To clearly see how these metrics relate with each other, a correlation matrix was produced (taking out the Country and Year fields from the set).

![alt text](https://github.com/jords-santiago/humans_are_pollutants/blob/main/99_Pictures/corr_overall.png "Correlation - Overall") 

Also, to get more detail, correlation matrices were produced for these countries:

United States:

![alt text](https://github.com/jords-santiago/humans_are_pollutants/blob/main/99_Pictures/corr_USA.png "Correlation - United States") 

Japan:

![alt text](https://github.com/jords-santiago/humans_are_pollutants/blob/main/99_Pictures/corr_JAPAN.png "Correlation - Japan") 

India:

![alt text](https://github.com/jords-santiago/humans_are_pollutants/blob/main/99_Pictures/corr_INDIA.png "Correlation - India") 

## Conclusions

In general, the data shows that gas emissions and air pollution increase along with the development indicators like population growth and GDP.  These 5 countries are among the most developed in the world thus the GDP and population.  Also, the data only span from 2010 to 2017 as this the time period that the data gathered have in common but seems not enough to find a significant trend.

On the other hand, Forest Area being negatively correlated with gas emissions and pollution may be something worth looking further into as most countries in the set have this trend.

## Recommendations

Overall, it may be better to find trends on this on a per country basis instead of finding out trends on multiple countries.  Cultures may play a role on how each country address any environment issues and natural calamities are not the same in all countries.

At this analysis, however, Forest Area seems to be significant to having less gas emissions and pollution.  Looking further into data on reforestation and even tree conditions (e.g. there maybe a lot of forests in California but significant parts of those are "dead trees" that would just be fuel to forest fires) would give further detail if those definitely help address the environment.  This kind of data are usually found in GIS (Geographic Information System) databases which have a different way of processing/preparation before it can be analyzed in this manner.
