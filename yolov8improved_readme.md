# YOLOv8 Modification

## Overview
This project is a modified version of [YOLOv8](https://github.com/ultralytics/ultralytics), designed for automated diagnosis of lung cancer from CT scans.  
It is based on the research: *"An Automated Diagnosis Method for Lung Cancer Target Detection and Subtype Classification-Based CT Scans"*.
The main goal is to provide an easy-to-integrate modification for YOLOv8 to enhance lung cancer detection and subtype classification.

The improvements include integration of a large separable kernel attention mechanism in the C2f module to focus on key lung cancer features, enhancement of the SPPF module using depth-wise convolution with coordinate attention to increase receptive field and feature retention, and replacement of CIOU Loss with MPDIOU Loss for more precise bounding box localization and subtype recognition.

---

## Features
- Modified YOLOv8 architecture tailored for lung cancer target detection.
- Attention mechanisms in Backbone and Neck for improved feature representation.
- Enhanced SPPF module for better perception of various lung cancer shapes.
---

## Installation

1. Clone or install the original [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) repository.
2. Replace the following files/folders in the YOLOv8 repository with the ones in this project:

```
your_project/
├─ nn/
│ ├─ init.py → replace YOLOv8 nn/__init__.py
│ ├─ tasks.py → replace YOLOv8 nn/tasks.py
│ └─ module/ → replace YOLOv8 nn/module/
```

3. Ensure dependencies of YOLOv8 are installed:

```bash
pip install -r requirements.txt
```

---

## Usage

After replacing the files:

```python
from nn.module import your_module
# Example usage
```

Follow standard YOLOv8 training and inference procedures.  
Your model now incorporates the modified modules for lung cancer detection and classification.

---

## Project Structure

```
your_project/
├─ nn/
│  ├─ __init__.py      # Modified init
│  └─ module/          # Modified modules
├─ README.md
└─ requirements.txt
```

---

## References
- YOLOv8: [Ultralytics](https://github.com/ultralytics/ultralytics)  
- Lung Cancer Detection Research: *"An Automated Diagnosis Method for Lung Cancer Target Detection and Subtype Classification-Based CT Scans"* https://doi.org/10.3390/bioengineering11080767

---

## Notes
- This project only modifies YOLOv8 `nn` modules and loss function.  
- Make sure to backup original YOLOv8 files before replacing.  
- Compatible with latest YOLOv8 versions as of this project.

