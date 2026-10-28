# Series-16-Imports
R-based analysis and forecasting of Imports from Mexico for SANDAG's Series 16 Regional Economic Forecast.
Overview

This repository contains the R code and supporting analysis used to evaluate and update the forecast of imports from Mexico through the San Diego Customs District for SANDAG's Series 16 Regional Economic Forecast.

The analysis evaluates the performance of the previous Series 15 (SR15) imports forecast against observed monthly import data through September 2026, then reestimates the forecast using an ARIMA model. It also develops an alternative dampened ARIMA forecast to evaluate a more conservative long-term growth trajectory.

Methodology

1. Series 15 Forecast Evaluation

The analysis begins by comparing the SR15 forecast against observed import values to evaluate how well the previous model predicted actual imports, particularly during the period following the COVID-19 pandemic.

2. Updated ARIMA Forecast

An ARIMA(0,1,1) model with drift is estimated using historical monthly import data through December 2019. The model generates an updated forecast beginning in 2020, allowing its performance to be compared against observed data and the previous SR15 forecast.

3. Dampened ARIMA Forecast

An alternative forecast is developed to evaluate the implications of moderating the ARIMA model's long-term growth.

Rather than assuming the annual dollar increase projected by ARIMA continues indefinitely, the dampened model gradually transitions toward the historical average annual increase observed between 2007 and 2019.

The model preserves the full ARIMA-implied annual increase through 2030. Beginning in 2031, an exponential decay function gradually reduces the difference between the ARIMA and historical annual increases.

Sensitivity testing is used to evaluate different rates of convergence and select an appropriate adjustment parameter.

4. Economic Adjustment Scenarios

Additional scenarios incorporate near-term economic growth assumptions before returning to the ARIMA or dampened ARIMA annual increases over the longer term.

Outputs

The analysis produces:

Comparisons of the SR15 forecast, updated ARIMA forecast, and observed import values.

Annual import forecasts through 2060.

Alternative dampened ARIMA forecasts.

Economic adjustment scenarios.

Sensitivity analysis of alternative dampening parameters.

CSV outputs and figures documenting forecast assumptions and results.

Data Source

USA Trade Online, U.S. Census Bureau — Monthly imports from Mexico through the San Diego Customs District.

Historical data cover January 2001 through September 2026.

Purpose

The analysis supports the development of SANDAG's Series 16 Regional Economic Forecast by evaluating the performance of the previous imports forecast, updating the underlying statistical model, and exploring alternative assumptions about long-term import growth.
