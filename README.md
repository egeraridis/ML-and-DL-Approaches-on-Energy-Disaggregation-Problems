# Energy Disaggregation using Machine Learning Approaches

## Overview
Effective energy management is one of the most critical issues of our time. Energy production remains a polluting and costly process, with approximately 80% still provided by non-renewable sources, even in developed countries. By knowing how much energy each household appliance consumes individually, consumers can save money by reducing the use of energy-intensive devices and simultaneously reduce their carbon footprint.

For energy providers, understanding the energy needs in advance helps avoid unnecessary production and potential grid overload due to increased demand. Additionally, users can detect malfunctioning devices through their individual consumption data, which may indicate potential failures.

## Problem Statement
A practical approach to accurately measure the energy consumption of each household appliance involves installing a meter on each device and recording consumption periodically. However, this solution is both costly and challenging to implement, as it requires multiple meters in each household, increasing the likelihood of meter failures over time.

## Solution
Leveraging today's computational advancements, this problem can be more effectively addressed using machine learning methods. By utilizing a single central meter per household, we can derive accurate insights into the consumption of individual household appliances. This approach not only reduces costs but also enhances reliability, as it requires monitoring only one central meter's functionality.

## Objectives
The objective of this thesis is to develop and compare machine learning models to predict the energy needs of each device and the household as a whole. By doing so, we aim to provide a more efficient and cost-effective solution for energy disaggregation.


## Datasets used:

- ENERTALK:

The ENERTALK dataset comprises data collected in South Korea from twenty-two households. The data collection duration varied from twenty-nine to one hundred twenty-two days (29-122 days) depending on the household, with a constant sampling rate of 15 Hz. This sampling rate applied to both the overall household meter and all individual appliance meters within each household. 

The meters used to collect the data were the ENERTALK and ENERTALK PLUS, which operate within a voltage range of 100-240V. These meters accumulate power signals at 7.8125 kHz within the integrated measurement circuits and then down-sample to 15 Hz.

- REDD:

The REDD (Reference Energy Disaggregation Data Set) is a publicly available dataset collected around 2011 with the primary goal of advancing research in energy disaggregation. The REDD dataset contains detailed information on energy usage from various households, including both high-frequency (kHz) and low-frequency (Hz) data, such as current and voltage measurements. 

It is noteworthy that the REDD dataset was the first openly available dataset developed specifically for research in this field, serving as a reference point for scientific studies to this day.


- MEAZON:

For the purposes of this thesis, two datasets from Meazon were used. These datasets were collected using a smart meter that monitors the aggregate power of a household unit on phase A and the water heater on phase C, as well as data from individual meters that monitor various household appliances (microwave, refrigerator, washing machine, electric stove, dishwasher). The datasets consist of records collected during September 2022 and the first half of October 2022. These files are in CSV (Comma-Separated Values) format and contain five variables: active power, apparent power, current, voltage, and peak factor for each of the available devices as well as for the total signal.

The data is transmitted at a frequency determined by the levels of active power. Generally, under normal conditions when the active power is stable, data is transmitted at a frequency of 1 sample per minute. When the power exceeds a threshold of 100 watts, the meter begins transmitting data at a frequency of 1 sample every 50 milliseconds. Additionally, when the current power compared to the last transmitted power exceeds a lower threshold, high-frequency mode is activated. This high-frequency transmission lasts for three seconds, after which the meter returns to low-frequency mode (1 sample per minute).



## Algorithms & Models Implemented:

- Gradient Boosted Trees via PySpark API.
  
- Random Forest Trees via PySpark API.
  
- Simple Linear Regression Models (mostly to compare results to the more sophisticated methods used), using PySpark API.
  
- Recurrent Neural Networks using LSTM's and GRU's (both in one network or in separate ones).
  
- NILMTK Algorithms (Combinatorial Optimization, Hart_85) on the REDD Dataset (since necessary metadata were available).
  
- Approximation Algorithms on the datasets where metadata were not available (ENERTALK & MEAZON) by using k-means and k-NN.

*Note: PySpark was used for better scalability for future work purposes mostly.


<img src="https://github.com/user-attachments/assets/d2c40ddd-ca2f-4c07-975a-a66d0452c61f" alt="Description of image" width="200" height="200">
<img src="https://github.com/user-attachments/assets/436e1479-b411-44b8-b237-7eb6003e7ced" alt="Desc' width="300" height="300">
