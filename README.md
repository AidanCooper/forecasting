# Forecasting Techniques Comparison

## Introduction

Performance comparison of various time series forecasting techniques, including deep learning methods, presented as Python implemenations in Jupyter notebooks. These notebooks are written so that they can be read and understood in isolation, and as such, there may be repetition in certain parts between them. The models presented are by no means fully optimised, but are intended to serve as a framework for anyone interested in implementing these forecasting techniques in their own projects.

This repository is actively being updated with more forecasting methods and datasets.

## Forecasting Techniques

The forecasting techniques demonstrated in this repository are as follows:
- [Average Method](Average) - A simple benchmark model<sup>1</sup>
- [Seasonal Naïve Method](Naive) - A simple benchmark model<sup>1</sup>
- [Linear Regression](LinearRegression)
- [ARIMA](ARIMA)<sup>2</sup>
- [ARIMAX](ARIMAX)<sup>2</sup>
- [SARIMA](SARIMA)<sup>2</sup>
- [SARIMAX](SARIMAX)<sup>2</sup>
- [Prophet](Prophet) - An open source time series forecasting method from Facebook<sup>3</sup>
- [SageMaker DeepAR](DeepAR) - A deep learning method on the AWS SageMaker platform<sup>4</sup>

## Datasets

Datasets that exhibit seasonality, and those that don't, are treated separately.

**Seasonal Datasets:**
- [California Solar Power](datasets/california-solar-power.ipynb) (CSP) - Power output of 405 photovoltaic power stations at five minute intervals<sup>5</sup>
- [Household Electricity Consumption](datasets/household-electricity-consumption.ipynb) (HEC) - Electricity consumption of 370 households in Portugal at 15 minute intervals<sup>6</sup>

**Non-Seasonal Datasets:**
- N/A

## Evaluation

For non-seasonal datasets (currently none), the *mean absolute scaled error* (MASE)<sup>7</sup> is used to evaluate and compare forecasting accuracies for the different techniques. For seasonal datasets (currently CSP and HEC), the seasonal variant (sMASE) is used.

## Results

The results are shown below and are also viewable in [this notebook](model-performance-comparisons.ipynb).

**Seasonal Datasets:**

||CSP | HEC
|---|---|---|
|SARIMA | 0.734733 | 1.60976
|SARIMAX | 0.75265 | 1.61433
|Naive | 1 | 1
|DeepAR | 1.0884 | 1.69218
|Prophet | 1.10443 | 1.63378
|LinearRegression | 1.46422 | 2.03795
|ARIMA | 3.14786 | 2.04262
|ARIMAX | 3.62378 | 2.01298
|Average | 5.20921 | 2.39973


**Non-Seasonal Datasets:**

N/A

---
#### References:<br>
1: [Forecasting: Principles and Practice](https://otexts.org/fpp2/simple-methods.html)<br>
2: [Autoregressive integrated moving average (Wikipedia)](https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average)<br>
3: [facebook prophet](https://github.com/facebook/prophet)<br>
4: [Amazon SageMaker DeepAR Forecasting](https://docs.aws.amazon.com/sagemaker/latest/dg/deepar.html)<br>
5: [National Renewable Energy Laboratory](https://www.nrel.gov/grid/solar-power-data.html)<br>
6: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/ElectricityLoadDiagrams20112014)<br>
7: [Forecasting: Principles and Practice - Chapter 3.4](https://otexts.org/fpp2/accuracy.html)<br>
