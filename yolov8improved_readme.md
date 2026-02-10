# YOLOv8 Modification

## Overview
This project is a modified version of [YOLOv8](https://github.com/ultralytics/ultralytics), designed for automated diagnosis of lung cancer from CT scans.  
It is based on the research: *"An Automated Diagnosis Method for Lung Cancer Target Detection and Subtype Classification-Based CT Scans"*.

The main goal is to provide an easy-to-integrate modification for YOLOv8 to enhance lung cancer detection and subtype classification.

---

## Features
- Modified YOLOv8 architecture tailored for lung cancer target detection.
- Supports subtype classification from CT scans.
- Easy integration: just replace specific YOLOv8 modules.

---

## Installation

1. Clone or install the original [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) repository.
2. Replace the following files/folders in the YOLOv8 repository with the ones in this project:

```
your_project/
├─ nn/
│  ├─ __init__.py  → replace YOLOv8 `nn/__init__.py`
│  └─ module/      → replace YOLOv8 `nn/module/`
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
- This project only modifies YOLOv8 `nn` modules.  
- Make sure to backup original YOLOv8 files before replacing.  
- Compatible with latest YOLOv8 versions as of this project.

