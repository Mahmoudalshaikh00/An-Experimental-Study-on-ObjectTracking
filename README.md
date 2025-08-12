# Repository Structure

This repository contains code and data for particle tracking using LSTM (Long Short-Term Memory) neural networks. Here's how the files and folders are organized:

## Main Folders

### 📁 `LSTM-model/`
This folder contains the trained LSTM model files:
- Model weights and parameters for different regions (left/right, 22 regions)
- Normalized model files for better performance
- These are the "brain" files that the AI uses to track particles

### 📁 `final output/`
This is where all the results are stored after running the tracking:

#### 📁 `GIF/`
- Contains animated GIF files showing particle trajectories
- Files like `PF.gif`, `byte55.gif` show the tracking results visually
- `traj_*.gif` files show different tracking methods (EKF, KF, true trajectories)

#### 📁 `JSON/`
- Contains data files in JSON format
- Stores tracking results, annotations, and analysis data
- Files like `3d_ann.json`, `EKF52_ann_final.json` contain the numerical results
- `box_list(kopia).pkl` contains bounding box information

#### 📁 `LSTM-model/` (subfolder)
- Additional model files used for final processing

### 📁 `.ipynb_checkpoints/`
- Automatic backup files created by Jupyter notebooks
- You can usually ignore this folder

## Main Files (Jupyter Notebooks)

These are the code files you can run:

- **`ByteTrack.ipynb`** - Implements ByteTrack algorithm for particle tracking
- **`KF&EKF.ipynb`** - Kalman Filter and Extended Kalman Filter implementations  
- **`LSTM-BEV.ipynb`** - LSTM model for Bird's Eye View tracking
- **`LSTM-train.ipynb`** - Code to train the LSTM models
- **`MOT-M.ipynb`** - Multi-Object Tracking implementation
- **`Particle Filter.ipynb`** - Particle Filter tracking algorithm

## Other Files

- **`.gitignore`** - Tells Git which files to ignore
- **`.DS_Store`** - System files (can be ignored)

## How to Use

1. Start with the training notebook (`LSTM-train.ipynb`) if you want to train your own models
2. Use the tracking notebooks (`ByteTrack.ipynb`, `KF&EKF.ipynb`, etc.) to run different tracking algorithms
3. Results will be saved in the `final output/` folder
4. Check the `GIF/` folder to see visual results of your tracking

## File Naming Convention

- Files with `EKF` = Extended Kalman Filter results
- Files with `KF` = Kalman Filter results  
- Files with `traj_` = Trajectory files
- Files with numbers (like `52`, `222`) = Different experimental runs or parameters
- Files ending in `_final` = Final processed results
