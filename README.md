# Repository Structure
## Main Folders

### 📁 `final output/`
This is where all the results are store d after running the tracking:

#### 📁 `GIF/`
- Contains animated GIF files showing particle trajectories
- Files like `PF.gif`, `byte55.gif` show the tracking results visually
- `traj_*.gif` files show different tracking methods EKF, KF, ByteTrack, PF and true trajectories

#### 📁 `JSON/`
- Contains data files in JSON format
- Stores tracking results, annotations, and analysis data
- Files like `3d_ann.json`, `EKF52_ann_final.json` contain the numerical results
- `box_list(kopia).pkl` contains bounding box information


## Main Files (Jupyter Notebooks)

These are the code files can run:

- **`ByteTrack.ipynb`** - Implements ByteTrack algorithm for particle tracking
- **`KF&EKF.ipynb`** - Kalman Filter and Extended Kalman Filter implementations  
- **`LSTM-BEV.ipynb`** - LSTM model for Bird's Eye View tracking
- **`LSTM-train.ipynb`** - Code to train the LSTM models
- **`MOT-M.ipynb`** - Multi-Object Tracking implementation
- **`Particle Filter.ipynb`** - Particle Filter tracking algorithm


### 📁 `LSTM-model/`
This folder contains the trained LSTM model files:
- Model weights and parameters for different regions (left/right, 22 regions)
- Normalized model files for better performance
- These are the "brain" files that the AI uses to track particles





