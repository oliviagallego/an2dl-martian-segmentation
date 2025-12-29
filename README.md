# Martian Terrain Segmentation (AN2DL HW2)

Semantic segmentation of Martian terrain with severe class imbalance (notably **class 4: large rocks**).

## What’s inside
- U-Net based model trained from scratch
- Augmentations (e.g., GridMask) + ablations
- Strategies for class imbalance (weights / sampling / cropping)
- Evaluation with Mean IoU + per-class analysis

## Repository
- `notebooks/01_preprocessing_with_split.ipynb` — preprocessing + split strategy
- `notebooks/02_training_unet.ipynb` — main training notebook
- `notebooks/03_combining_augmentations.ipynb` — augmentation experiments
- `report/AN2DL_Second_Homework.pdf` — final report
- `data/README.md` — how to place/generate data locally


## Results (from report)
Class imbalance was extreme (class 4 ~0.13% of pixels). The final model improved overall performance,
but class 4 IoU remained challenging (~9%), highlighting the difficulty of rare-class segmentation.

## How to run
1) Create environment
- `pip install -r requirements.txt`  (or use `environment.yml`)

2) Place dataset locally (see `data/README.md`)

3) Run notebooks in order:
- `01_preprocessing_with_split.ipynb`
- `02_training_unet.ipynb`

## Disclaimer
Educational project. Not for operational use.
