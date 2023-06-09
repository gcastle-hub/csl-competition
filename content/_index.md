---
title: Home
---

## Overview

In this competition, the goal is to solve a causal structure learning problem in AIOps (Artificial Intelligence for IT Operations). In telecommunication networks, anomalies are commonly identified through alarms. The network operators might be facing millions of alarms per day due to the large scale and the interrelated structure of the network, as a single fault in the network can trigger a flood of various types of alarms on multiple connected devices. The goal of the operators is to quickly localize the failure point to facilitate a fast repair and recovery. However, to handle all these alarms is exhausting and can quickly overwhelm the operators, and hence it must be done in an intelligent. Recently, there has been increasing interest in tackling the above root cause analysis (RCA) problem from a causal perspective, i.e., learning a causal graph that represents alarm relations and then using decision-making techniques (such as causal effect estimation and counterfactual inference) to efficiently identify the root cause alarm when a fault occurs. A typical RCA solution for the telecommunication network is depicted in Figure 1.

The competition task can be described as follows: Given a series of datasets, for each dataset, participants are supposed to use the historical alarm data, device topology, and prior knowledge (if available) to learn a causal graph for the involved alarm types. Each learned causal graph is represented by a binary adjacency matrix, where the element in the i-th row and j-th column of the matrix equals 1 (0) means the existence (resp. non-existence) of a directed edge from the alarm type i to alarm type j. The ground truth for these causal graphs, i.e. true causal graphs, are labeled manually by experts or, for the synthetic datasets, the pre-set causal assumptions. Please note that all true causal graphs will not be public during the competition. Besides, we recommend competitors design a unified learning solution(algorithm) for handling all datasets. While it’s not mandatory, the generalization of the submitted solution(algorithm) will be an important aspect of evaluating the novelty and will affect the final ranking.


![Figure 1](https://gcastle-hub.github.io/competions.github.io/assets/img/about-img.jpg)

##### Figure 1: RCA solution in a telecom network