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

## Algorithms & Models Implemented:

- Gradient Boosted Trees via PySpark API.
  
- Random Forest Trees via PySpark API.
  
- Simple Linear Regression Models (mostly to compare results to the more sophisticated methods used), using PySpark API.
  
- Recurrent Neural Networks using LSTM's and GRU's (both in one network or in separate ones).
  
- NILMTK Algorithms (Combinatorial Optimization, Hart_85) on the REDD Dataset (since necessary metadata were available).
  
- Approximation Algorithms on the datasets where metadata were not available (ENERTALK & MEAZON) by using k-means and k-NN.

*Note: PySpark was used for better scalability for future work purposes mostly.



