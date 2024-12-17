# **    Empowering Vision: Optimizing Object Detection with YOLOv8**

## **Project Overview**

This project implements an **Object Detection System** using the **YOLOv8** model to detect and classify objects from the **PASCAL VOC 2012 Dataset**. The project focuses on building a robust object detection pipeline with optimizations for performance and efficiency.

Key features include:

- **Baseline Training**: Train YOLOv8 with default parameters.
- **Data Augmentation**: Apply augmentation to improve generalization.
- **Hyperparameter Tuning**: Optimize key training parameters.
- **Mixed Precision Training**: Utilize AMP for computational efficiency.
- **Performance Visualization**: Visualize mAP, Precision, and Recall using charts.

---

## **Dataset**

The **PASCAL VOC 2012 Dataset** is used for this project. It contains annotated images with bounding boxes for multiple object classes.

- **Dataset Directory Structure**:
    ```
    PASCAL_VOC/
    ├── train/
    │   ├── images/
    │   ├── labels/
    ├── valid/
    │   ├── images/
    │   ├── labels/
    ```

### **Download Dataset**

You can use the dataset provided in the project directory **or** download it from **Roboflow**:

- [PASCAL VOC 2012 Dataset (Roboflow Link)](https://public.roboflow.com/ds/EQ8visPO3n?key=4Goqh4AXD4)

To download the dataset programmatically:

```python
import os
import requests
import zipfile

# Roboflow URL
url = "https://public.roboflow.com/ds/EQ8visPO3n?key=4Goqh4AXD4"
output_path = "pascal_voc.zip"

# Download the dataset
print("Downloading dataset...")
response = requests.get(url)
with open(output_path, "wb") as file:
    file.write(response.content)

# Extract the dataset
with zipfile.ZipFile(output_path, 'r') as zip_ref:
    zip_ref.extractall("PASCAL_VOC")
print("Dataset downloaded and extracted successfully.")
```
### **Installing Depedencies**
Install all the dependencies required to ru the code from the `requirements.txt` using
```
pip install -r requirements.txt
```
