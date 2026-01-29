# PPE-Detection-YOLOv11

Personal Protective Equipment (PPE) detection using YOLOv11-L for construction
safety monitoring.

## Dataset
Experiments were conducted on the CHVG (HCVG) dataset consisting of 1,699 images.
The dataset was prepared using Roboflow with auto-orientation enabled and all
images resized to 640×640 pixels.

Dataset split:
- Training: 1,188 images (70%)
- Validation: 340 images (20%)
- Test: 171 images (10%)

## Model and Training
- Architecture: YOLOv11-L (Ultralytics)
- Input resolution: 640×640
- Epochs: 100
- Batch size: 16
- Optimizer: AdamW (auto-selected by Ultralytics)
- Initial learning rate: 8.33e-4
- Momentum: 0.9
- Weight decay: 5e-4
- Random seed: 0
- Mixed precision (AMP): enabled

## Computational Resources
Training and evaluation were performed using Google Colab with a temporary
NVIDIA Tesla T4 GPU. No dedicated local GPU resources were used.

## Results
The YOLOv11-L model achieved:
- mAP@0.5: 94.4%
- mAP@0.5:0.95: 63.1%

Evaluation results, precision–recall curves, and confusion matrices are provided
in the `results_yolov11_ppe.zip` file.

## Reproducibility
The full training and evaluation pipeline is provided in the Google Colab
notebook:
- `train_yolov11_ppe_colab.ipynb`

All experiments can be reproduced by running the notebook with the specified
dependencies.

## Framework Versions
- Ultralytics: 8.3.221
- Python: 3.12.12
- PyTorch: 2.8.0 + CUDA 12.6
- GPU: NVIDIA Tesla T4
