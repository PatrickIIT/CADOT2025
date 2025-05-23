# CADOT2025

# Create README.md
readme_content = """
# TeamName_CADOT_Challenge

## Hardware/Software Requirements
- Hardware: NVIDIA A100 GPU, 40GB VRAM
- Software: Ubuntu 20.04, CUDA 12.0, Python 3.11
- Dependencies: See requirements.txt

## Execution Commands
1. Install dependencies: `pip install -r requirements.txt`
2. Run training and evaluation: `python cadot_yolo_comparison.py`
3. Generate test predictions: Outputs saved to `results/{model}_predictions.json`

## Validation Scores
See `results/metrics.csv` for mAP@50 and per-class AP scores.

## Directory Structure
- `data/`: Instructions in instructions.md
- `models/`: Trained weights (cadot_yolov5.pt, cadot_yolov8.pt, cadot_yolov11.pt)
- `scripts/`: cadot_yolo_comparison.py
- `results/`: metrics.csv, predictions.json
- `reports/`: convergence_plot.png, confusion_matrix.png, report.pdf
"""
with open(os.path.join(output_dir, "README.md"), "w") as f:
    f.write(readme_content)

# Create requirements.txt
requirements_content = """
ultralytics==8.2.0
pycocotools==2.0.7
numpy==1.26.4
opencv-python==4.9.0.80
pyyaml==6.0.1
torch==2.1.0
pandas==2.2.2
matplotlib==3.8.4
"""
with open(os.path.join(output_dir, "requirements.txt"), "w") as f:
    f.write(requirements_content)

print("Repository files prepared at:", output_dir)
