# Dynamic Pricing for Urban Parking Lots

## Project Overview

This project demonstrates the implementation of a dynamic pricing system for urban parking lots using Python, real-time data streaming (Pathway), and data visualization (Bokeh). It improves parking efficiency by adjusting prices based on real-time occupancy, traffic, and competition.


## Problem Statement

Urban parking lots often suffer from inefficient pricing due to static rates. This project addresses that challenge by developing a real-time pricing engine that adapts to multiple parameters to optimize both utilization and revenue.


## Objectives

 Build and compare three pricing models:

  1. Linear Pricing

  2. Demand-Based Pricing

  3. Competitive Pricing

 Integrate real-time data processing using Pathway

 Simulate streaming data in Google Colab

 Visualize pricing outcomes with Bokeh

 Export results and perform statistical analysis for business decisions

## Dataset Description

The dataset consists of over 18,000 records from urban parking locations and includes the following features:

i. SystemCodeNumber

ii. Capacity and Occupancy

iii. QueueLength and VehicleType

iv. TrafficConditionNearby

v. IsSpecialDay

vi. Timestamp, Hour

## Models Implemented

#### Model 1: Linear Pricing

Formula: Price = Previous_Price + α × (Occupancy / Capacity)

Characteristics:

Simple linear growth based on occupancy

Bounded within min and max price

#### Model 2: Demand-Based Pricing

Factors: Occupancy Rate, Queue Length, Traffic Condition, Vehicle Type, Special Day

Formula: Price = Base_Price × (1 + λ × Normalized_Demand) × Vehicle_Weight

Captures realistic pricing behavior with weighted parameters

#### Model 3: Competitive Pricing

Proximity analysis using Haversine formula

Compares nearby competitor pricing

Suggests redirection when lots are full

Dynamically adjusts price based on market competition

## Implementation Highlights

i. Encapsulated in the DynamicParkingPricer class

ii. Real-time simulator: simulate_real_time()

iii. Pathway integration for live stream processing

iv. Exported processed data and price recommendations

## Visualizations

i. Bokeh dashboard for real-time price visualization

ii. Boxplot analysis by vehicle type

iii. Occupancy vs. Price trends

iv. Demand Score tracking



## Tools and Technologies

Languages: Python

Libraries: Pandas, NumPy, Bokeh, Matplotlib, Seaborn

Streaming: Pathway

Platform: Google Colab / Jupyter Notebook


## Insights

Vehicle Type Impact: Trucks incur ~50% higher fees than cars

Traffic Impact: High traffic raises prices by ~20%

Model 2 offers nuanced pricing over Model 1

Model 3 enhances competitiveness with location-aware pricing

## Configuration Parameters

base_price = 10.0
min_price = 5.0
max_price = 20.0
ALPHA = 5.0
TRAFFIC_MULTIPLIERS = {'low': 0.9, 'average': 1.0, 'high': 1.2}
VEHICLE_WEIGHTS = {'car': 1.0, 'truck': 1.5, 'bike': 0.7, 'cycle': 0.5}



## Exports and Summary

i. Exported results as CSV for analysis

ii. Boxplots and visual outputs support business review

iii. Structured notebook supports reproducibility



