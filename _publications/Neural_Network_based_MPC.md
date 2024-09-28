---
title: "Neural Network-Based Model Predictive Control for CSTR: A Comparative Study of Output Layer Architectures "
collection: publications
permalink: /publication/Neural-network-based-Model-predictive-control
excerpt: 'In recent years, neural networks have proven to be valuable tools in improving Model Predictive Control (MPC) for complex systems. This study takes a close look at how neural networks can be used to model the dynamics of a Continuous Stirred Tank Reactor (CSTR), which is a common system in chemical processes. we explore how neural networks can serve as alternatives to traditional models in MPC, opening up new possibilities for combining advanced learning techniques with control systems. In this research we compare **MLPs** and **KANs** as a output layers architectures and using LSTM and GRU to handle time-serie data from dynamic of system.'
date: 2024-09-05
venue: 'https://mosi2002.github.io/home/'
citation: 'In Preparation'
---
In recent years, neural networks have proven to be valuable tools in improving Model Predictive Control (MPC) for complex systems. This study takes a close look at how neural networks can be used to model the dynamics of a Continuous Stirred Tank Reactor (CSTR), which is a common system in chemical processes. we explore how neural networks can serve as alternatives to traditional models in MPC, opening up new possibilities for combining advanced learning techniques with control systems. In this research we compare **MLPs** and **KANs** as a output layers architectures and using LSTM and GRU to handle time-serie data from dynamic of system.

Gated Recurrent Units (GRUs) are a type of Recurrent Neural Network (RNN) that are particularly well-suited for processing **time series** data. GRUs are computationally less expensive than their counterparts, such as Long Short-Term Memory (LSTM) networks, while still offering comparable performance. This efficiency is crucial in real-time control systems where quick decisions are necessary.

The states for CSTR are $$C_A$$ and $$T$$. The control inputs are $$C_A0$$ and $$Q$$. Next Step is about initializing random states and control inputs and obtain the outputs from dynamic of CSTR:

$$
\frac{dC_A}{dt} = \frac{F}{V}(C_{A0} - C_A) - k_0 e^{-\frac{E}{RT}} C_A^2 \\
\frac{dT}{dt} = \frac{F}{V}(T_0 - T) + \frac{-\Delta H}{\rho_L C_P} k_0 e^{-\frac{E}{RT}} C_A^2 + \frac{Q}{\rho_L C_P V}
$$

then By Concatenation of all the these inputs and the outputs N samples over time and it can be used for LSTM or GRU model. In this article we focuse on comparison study on output layers of these models and we compare **MLPs** and **KANs**.

**Pleased to announce that my latest project, conducted in collaboration with [S. Vahid Naghvi](https://scholar.google.com/citations?user=5bT9h5IAAAAJ&hl=en), is nearing its release. This study explores the application of neural network-based model predictive control (MPC) for a Continuous Stirred Tank Reactor (CSTR).

