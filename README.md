# CADOT2025

# Nebula_CADOT_Challenge

## Hardware/Software Requirements
- Hardware: NVIDIA A100 GPU, 40GB VRAM
- Software: Ubuntu 20.04, CUDA 12.1, Python 3.11
- Dependencies: See requirements.txt

## Execution Commands
1. Install dependencies: `pip install -r requirements.txt`
2. Run training and evaluation: `python cadot_yolov11_regression.py`
3. Generate test predictions: Outputs saved to `results/yolov11m_predictions.json`

## Validation Scores
See `results/metrics.csv` for mAP@50 and per-class AP scores.

## Visualizations
- `reports/train_annotated_images.png`: Sample images with annotations.
- `reports/class_distribution.png`: Class distribution histogram.
- `reports/iou_distribution.png`: IoU distribution of predictions.
- `reports/confusion_matrix.png`: Confusion matrix.

## Directory Structure
- `data/`: Instructions in instructions.md
- `models/`: Trained weights (cadot_yolov11.pt)
- `scripts/`: cadot_yolov11_regression.py
- `results/`: metrics.csv, yolov11m_predictions.json
- `reports/`: visualizations, report.pdf
"""
with open(os.path.join(output_dir, "README.md"), "w") as f:
    f.write(readme_content)

# Create requirements.txt
requirements_content = """
ultralytics==8.2.10
pycocotools==2.0.7
numpy==1.26.4
opencv-python==4.10.0.84
pyyaml==6.0.1
matplotlib==3.8.4
pandas==2.2.2
torch==2.1.0+cu121
torchvision==0.16.0+cu121
scipy==1.13.1
requests==2.32.3
"""e(requirements_content)

print("Repository files prepared at:", output_dir)
