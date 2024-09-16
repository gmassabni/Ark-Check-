# Ark-Check-
An automated tool designed to review and analyze architecture drawings for potential drafting errors and compliance with design standards.

Project Name: Ark{Check}

An automated tool designed to review and analyze architecture drawings for potential drafting errors and compliance with design standards.

Table of Contents

Overview
Features
Installation
Usage
Model Training
Contributing
License
Contact

Overview

ArchInspect is a cutting-edge tool that leverages computer vision and machine learning to automatically identify drafting errors and design inconsistencies in architectural drawings. By automating the review process, it helps architects, engineers, and designers ensure their drawings meet quality standards, reducing manual checks and improving workflow efficiency.

Features

Automated detection of common drafting errors (e.g., misaligned walls, incorrect annotations).
Supports custom rule-based checks for adherence to project-specific guidelines.
Export error reports with annotated images and error descriptions.

Installation

To get started with ArkCheck, follow the steps below:
Clone the repository:
bash
Copy code
git clone https://github.com/gmassabni/Ark-Check.git
cd archinspect
Install the required dependencies:


## Dependencies

The project depends on the following libraries:

### **1. General Python Libraries**:
- `os`: For handling file operations.
- `random`: For generating random values, useful for splitting datasets.
- `shutil`: For file operations like copying or moving files.
- `xml.etree.ElementTree`: For parsing XML files.

### **2. Computer Vision Libraries**:
- `cv2 (OpenCV)`: For image processing and manipulation.
- `PIL (Pillow)`: For handling image file operations.
- `numpy`: For numerical operations.

### **3. Deep Learning Libraries**:
- `torch (PyTorch)`: For building and running neural networks.
- `ultralytics`: For using YOLOv8 from Ultralytics.
- `torchvision`: For image transformations.

### **4. Data Handling & Visualization**:
- `matplotlib`: For plotting and visualizing data.
- `pandas`: For data manipulation and analysis.
- `seaborn`: For statistical data visualization.

### **5. API Integration**:
- `replicate`: For using external APIs to enhance the project functionality.

### **6. UI Tools**:
- `gradio`: For creating a user-friendly web interface to interact with models.

## Usage

Once all the dependencies are installed, you can run the YOLOv5/YOLOv8 models and use Gradio for interacting with the models.

```bash
# Run YOLOv5 model
python detect.py --source ...

# Run YOLOv8 model
from ultralytics import YOLO
model = YOLO('yolov8n.pt')
```

### Gradio Interface
You can integrate a Gradio interface for easier interaction:

```python
import gradio as gr
def inference(img):
    # Your model inference code
    return result

gr.Interface(fn=inference, inputs="image", outputs="label").launch()
```

## Model Information

This project supports both YOLOv5 and YOLOv8 models. You can switch between them by adjusting the model loading part of the code.

- **YOLOv5**: Cloned from [ultralytics/yolov5](https://github.com/ultralytics/yolov5).
- **YOLOv8**: Integrated through the `ultralytics` library for easier deployment and usage
