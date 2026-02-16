# Pepper Growth Maturity Estimator

## Overview

This project attempts to use publicly available weather data and simple models to predict if a variety of pepper (*Capsicum* sp.) is able to reach maturity in a given period of time. The time to harvest the first mature fruits of a pepper plant is based not only on variety/heat level, but also temperature, light exposure, and irrigation. The goal is to find historical weather data for recorded control plantings, and then estimate time to maturity based on new weather data.

## Data Sources and Preparation

**Field Study:** The [CROPtime model](https://smallfarms.oregonstate.edu/smallfarms/crops/croptime) developed by the Oregon State University extension.

**Hothouse Study:** *The effects of temperature on flowering, fruit set and fruit development of glasshouse sweet pepper (Capsicum annuum L.)*, published in the Journal of Horticultural Science in 1989.

**Data Preparation:** The process of converting the raw data to training/testing/validation data is detailed in the Jupyter notebooks located in the **/notebooks/** directory in this repository. 

## Models

## Installation and Setup

**Dependencies:**
- Jupyter Labs
- Pandas

**Install steps**


## Usage

The script will take a location, historical start date (usually last Spring frost), historical end date (usually first fall frost), and a pepper variety/species. The script will pull the location's weather data for the specified period, and determine how many days of growth the crop is likely to receive during this period (*without calculating the growing degree days*). The estimated number of days to maturity will be output alongside the number of days in the given period, allowing the user to decide whether they can harvest a mature crop before the end of the season. 

## Limitations

**Maturity Data:** I could only find two published studies that listed the variety grown, the conditions or field location, *AND* days to first harvest of mature fruit. The lack of data is most likely due to how both sweet and hot peppers are grown. Most fruit, whether grown in hothouses or a field, are picked at a very unripe stage so that they maintain their green color in the market.

**Weather Data:** Additionally, the field studies only provided a rough location (within ~100 miles) of the measured plots, which complicates pulling the recorded weather data from the nearest weather station. As a result, the historical data for the field studies will need to be synthesized by pulling the yearly data for a weather station designated as a proxy for the field. The historical temperature data for hothouse studies can be easily replicated as the day and night temperatures are constant, but precipitation will be 0 mm for the growth period as these crops are bottom irrigated and thus soil, leaf canopy, and humidity data do not have the same effects as field-grown peppers.