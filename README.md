# Joint-Spatio-Temporal-Self-Supervised-Learning
**JST-SSL** is a self-supervised framework that learns strong, reliable features from unlabeled LiDAR sequences by combining spatial context and temporal consistency. It lets object detectors capture motion-aware and context-rich embeddings without any labeled data, boosting both precise localization and accurate classification. On a warehouse LiDAR dataset (3,287 scans, five industrial objects), it delivers excellent results: average center error of 0.20 m, size error of 0.19 m, and impressive per-class mAP@0.5 (FTS 0.99, Forklift 0.985, ELF++ 0.972, CargoBike 0.968, Box 0.901). Plus, it runs in real time at 271 FPS with only ~3 GMACs. It handles small or occluded objects much better, stays consistent in tricky warehouse scenes, and outperforms both supervised baselines and earlier self-supervised methods—especially in sparse or cluttered environments. Looking ahead, the team plans to add adaptive weighting of spatial/temporal cues, fuse in RGB or depth data, and create lighter models for edge devices to further improve small-object detection, cross-domain generalization, and long-term stability.

- mAP@0.5:  
  - FTS = 0.990  
  - ForkLift = 0.985  
  - ELFplusplus ≈ 0.972  
  - CargoBike ≈ 0.968  
  - Box = 0.901

---

# Key Features

- Joint spatio-temporal self-supervised pretraining  
- Hybrid geometric + contrastive learning  
- Detector-agnostic (compatible with SSD3D, VoteNet, YOLO3D, etc.)  
- Extremely robust to sparsity, occlusions, and industrial clutter  
- Real-time inference suitable for industrial automation

---

# Dataset

The Warehouse LiDAR Dataset is used for evaluation:  
https://github.com/anavsgmbh/lidar-warehouse-dataset

---

## Code

### Baselines

- 3DSSD: https://www.kaggle.com/code/mrifatrashid/3dlidar-3dssd-baseline-new-run
- VoteNet: https://www.kaggle.com/code/mrifatrashid/3dlidar-votenet-baseline-new-run 
- YOLO3D: https://www.kaggle.com/code/mrifatrashid/3dlidar-yolo3d-baseline-fixed-code

### SSLs

- BYOL + VoteNet: https://www.kaggle.com/code/rifat963/3dlidar-x-byol-votenet
- BYOL + YOLO3D and SSD3D: https://www.kaggle.com/code/rifat963/3dlidar-byol-yolo3d-ssd3d
- MAE + Baselines: https://www.kaggle.com/code/rifat963/3dlidar-mae-x-baselines
- SimCLR + Baselines: https://www.kaggle.com/code/rifat963/3dlidar-simclrxbaselines

### Proposed Approach
- JST-SSL: https://www.kaggle.com/code/kaziferdoushasan27/jst-ssl


