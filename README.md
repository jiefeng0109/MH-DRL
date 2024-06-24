# MH-DRL
    Multi-agent Deep Reinforcement Learning for Hyperspectral Band Selection with Hybrid Teacher Guide Knowledge-Based Systems
    Jie Feng *, Qiyang Gao , Ronghua Shang , Xianghai Cao , Gaiqin Bai , Xiangrong Zhang , Licheng Jiao

- [论文地址](https://www.sciencedirect.com/science/article/pii/S0950705124006786)
- [GitHub主页](https://github.com/jiefeng0109)
- [Jie Feng主页](https://github.com/jiefeng0109](https://web.xidian.edu.cn/fengjie/))

# Introduction
## A B S T R A C T
Due to the presence of noisy and highly redundant bands in hyperspectral images (HSIs), band selection serves as a key preprocessing for downstream classification tasks. Recently, deep reinforcement learning (DRL) has been developed as a new trend for band selection of HSIs. Existing DRL-based methods often adopt single-agent, which are prone to fall into local optima due to an excessive action space. The multi-agent methods provide a feasible solution, but often require too much computation. To address these problems, a novel multi-agent DRL method with hybrid teacher guide (MH-DRL) is proposed for band selection of HSIs. In MH-DRL, each agent corre-sponding to a spectral band decides whether this band is selected. Moreover, a presentation-evaluation network (PE-Net) is constructed to design the reward by evaluating the candidate band subsets without any fine-tuning and represent the state by extracting the spatial-spectral features of HSIs. Then, three kinds of experienced band selection models are regarded as the teachers and designed to participate in the band exploration of DRL, which can improve the learning effectiveness and efficiency by accumulating the external knowledge from diverse teacher models. Finally, deep Q-learning algorithm is designed to update the agents and improve their selflearning ability from continuous exploration. Experimental results on three widely-used HSI data verify the performance of the proposed method better than some advanced band selection algorithms of HSIs.

## Fig. 1. The framework of the proposed MH-DRL method. The red bands mean the selected bands while the grey one denotes the unselect band.
![image](https://github.com/jiefeng0109/MH-DRL/assets/26159369/c97aaa5f-deac-4e49-a801-8d5a8ca2ff1c)

## Fig. 3. The framework of designed deep Q-network.
![image](https://github.com/jiefeng0109/MH-DRL/assets/26159369/a7d7812e-7630-4dd1-8280-c095cfd2fd7f)

For further details, please check out our [paper](https://www.sciencedirect.com/science/article/pii/S0950705124006786). 

# Datasets

This repository provides access to three popular high-spectral image datasets used for remote sensing and classification tasks: Indian Pines, Pavia University, and Houston.

## Indian Pines

- **Download Address:** [Indian Pines Dataset](http://www.ehu.eus/ccwintco/uploads/6/67/Indian_pines_corrected.mat)
- **Ground Truth:** [Indian Pines Ground Truth](http://www.ehu.eus/ccwintco/uploads/c/c4/Indian_pines_gt.mat)

## Pavia University

- **Download Address:** [Pavia University Dataset](http://www.ehu.eus/ccwintco/uploads/e/ee/PaviaU.mat)
- **Ground Truth:** [Pavia University Ground Truth](http://www.ehu.eus/ccwintco/uploads/5/50/PaviaU_gt.mat)

## Houston

- **Download Address:** [Houston Dataset](http://hyperspectral.ee.uh.edu/?page_id=1076)
- **Ground Truth:** [Houston Ground Truth](http://hyperspectral.ee.uh.edu/?page_id=1076)

## Usage

To use these datasets, download the files from the provided links and load them into your hyperspectral image processing pipeline. Make sure to refer to the respective papers and sources for any specific preprocessing steps required.

# Code Structure and Execution Guide

This repository contains various scripts and modules for training and evaluating neural networks, including 3D CNNs and adaptive feature selection (AFS) techniques.

## Code Structure

### 3DCNN
- Implementation and training of 3D Convolutional Neural Networks.

### AFS (Adaptive Feature Selection)
- **ActionTeacher.py**: Script for substitutable teacher (advisor) in AFS.
- **Evaluate_Net.py**: Script for training and evolving the network.
- **main.py**: Main script for AFS network training.

### AutoFs
- Implementation of automatic feature selection algorithms.

### band_map
- Scripts related to band mapping for hyperspectral images.

### Classification_network
- **Evaluate_Net.py**: Script for training and evolving the classification network.
- **main.py**: Main script for training the classification network.

### Constrast_algorithm
- Scripts for contrast enhancement algorithms.

## Script Execution

To train and evaluate the networks, follow the instructions below:

### Training Evaluation Network

```bash
# Train evaluation network for 3DCNN
run Classification_network/3DCNN/Evaluate_Net.py

# Train evaluation network for AFS
run AFS/Evaluate_Net.py


