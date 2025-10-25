# Satellite Segmentation with U-Net (PyTorch)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/YOUR_USERNAME/satellite-segmentation-unet/blob/main/notebooks/main.ipynb
)

Semantic segmentation of satellite imagery using a compact U-Net.  
This repo includes a synthetic dataset so you can **run training immediately** in Colab.
Replace with real satellite tiles & masks to target land cover or deforestation.

## Quick start (Colab)
1. Open the notebook via the badge above.
2. Runtime → GPU.
3. Run all cells (training takes a few minutes on the tiny demo).
4. See qualitative predictions in the last cell.

## Data
- **Demo:** synthetic tiles generated in-notebook (`data/images/*.png`, `data/masks/*.png`).
- **Real data:** place satellite tiles in `data/images/` and corresponding binary masks in `data/masks/`.

## Model
- U-Net (encoder–decoder with skip connections), binary segmentation (1 class).
- Loss: `BCEWithLogitsLoss`, metric: mean IoU.

## Results (demo)
- Trains ~10 epochs on synthetic data; shows validation loss and mIoU.
- Displays 3 sample predictions (image, mask, prediction).

## Roadmap
- Multi-class segmentation (change `out_c`, loss, metrics).
- Real datasets (e.g., LandCover.ai, Sentinel-2 derived tiles).
- Augmentations (albumentations), learning rate scheduling, mixed precision.

## Environment
See `requirements.txt`.

## License
MIT
