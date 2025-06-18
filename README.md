This repository provides a Python implementation of the MCOTM algorithm (Mobility-aware Computation Offloading and Task Migration) for Wireless-Powered Mobile-Edge Computing in IIoT environments. It combines trajectory prediction, resource forecasting, and deep reinforcement learning (DDPG) to optimize task offloading and migration decisions.

About This Project:

MCOTM builds on the DDPG algorithm  and further improves adaptability to mobile edge environments by:

* Predicting device trajectories using Lagrange interpolation
* Forecasting server resource availability via LSTM
* Using DDPG to make intelligent online decisions for:

       * Offloading
       * Task migration
       * Resource allocation
  
Dataset:

This project uses real-world data from the Alibaba Cluster Trace Program:
Dataset: Alibaba Cluster Trace v2018
Usage: Extracted CPU, GPU, and Memory usage metrics were preprocessed and stored as updated_pod_list.csv for LSTM-based prediction
License: See Alibaba Cluster Trace repository for terms of use.
The dataset enables realistic modeling of edge server resource fluctuation for accurate LSTM training.

Requirements:

Install required packages:

* pip install tensorflow numpy scipy pandas matplotlib scikit-learn
This code uses TensorFlow 2.x.

How to Run
* pythin lagrange_mcotm.py
  
This will:

  * Load and preprocess system resource data
  * Train an LSTM to predict edge server resources
  * Simulate IIoT devices moving in a 2D space
  * Make offloading/migration decisions using DDPG
  * Print metrics: task turnaround time, energy usage, and migration rate.
  
Features:

 * LSTM for resource prediction
 * Lagrange interpolation for mobility/trajectory prediction
 * DDPG for smart offloading, migration, and allocation decisions
 * Cost-aware task migration to minimize delay and energy
 * Fully configurable for IIoT environments
 * Improved performance over traditional offloading
   
MCOTM achieves:

  ↓ At least 42% reduction in turnaround time
  ↓ Around 10% lower energy consumption
  ↓ Maintains task migration rate at ~50%
compared to baseline or static offloading schemes like greedy, DQN, or naive methods.

Reference Paper:

MCOTM: Mobility-aware Computation Offloading and Task Migration for Edge Computing in Industrial IoT
Wei Qin, Haiming Chen, Lei Wang, Yinshui Xia, Alfredo Nascita, Antonio Pescapè
Future Generation Computer Systems, Vol. 151, 2024, 


