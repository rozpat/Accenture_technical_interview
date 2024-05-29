# Overview

This repository contains functions for synchronising and processing data from Vicon, treadmill, and accelerometer datasets. The primary goal is to detect and align significant events (like peaks and local minima) across these datasets to enable accurate synchronisation.

These functions are a part of a bigger project that employed machine learning techniques to classify individuals’ states as either having their eyes opened or closed, based on Inertial Measurement Unit (IMU) data obtained from a smartphone’s gyroscope and accelerometer sensors. A CSV file was generated that serves as a resource for training machine learning models to accurately predict maximum Center of Pressure (CoP) values attainable during bending exercises. This forms the basis for a future analysis of the relative movement between CoP and CoM, enabling an assessment of postural and balance control to estimate the limits of stability

The motivation behind the main project is a desire to contribute to developing an innovative, artificial intelligence-based smartphone application designed to conduct an automated and comprehensive assessment of postural control.
The envisaged application will utilise the artificial intelligence model developed in
this project, enabling insights into the movement between the Centre of Pressure
(CoP) and the Centre of Mass (CoM) during quiet stance and walking in both,
normal and pathological populations.

To see more information about the project, use the following link: https://github.com/rozpat/dissertation_project.git

## Objective 1: Calculate statistics for the participants data
The function in participants_details.py folder is used to get insights into the studied population's characteristics. They include the number of male and female participants, the mean and standard deviation of various physical attributes such as age, height, weight, and more. 

## Objective 2: Data Synchronisation
The collection of functions from synchronisationv2.py file is designed to process and analyse signals from three disparate instruments- treadmill, VICON, and smartphone. These functions detect peaks, local minima, and compute accelerations. They are used to align the data from all mentioned instruments to ensure consistency in subsequent analyses.

## Objective 3: Event Detection 
The provided functions in event_detection.py automate the preprocessing, filtering, and analysis of CoP data, allowing for efficient detection of bending movements. The data can be then used to train the machine learning models.

## Python Files
- participants_details.py: The function calculates statistical data of the studied population
- synchronisation_v2.py: Functions synchronise all instruments based on VICON timestamps
- event_detection.py: Automates event detection (bending task) using the COP signal and generates data (e.g. timestamps) for further analysis
