# Underwater-Object-Detection-with-YOLO

This repository contains the code and resources for an object detection model trained to identify various marine organisms, including **fish**, **jellyfish**, and **starfish** and more, in underwater or aquarium environments.

### Google Colab Notebook

You can view and run the entire project directly using the provided notebook:

**[Open in Colab](https://colab.research.google.com/drive/1fT69gJyAz39IrlM2o4_y7fuaZ_Knwdfl?usp=sharing)**

---

## Demo Results

The model has been successfully trained and validated on diverse aquatic imagery, demonstrating accurate bounding box predictions and high confidence scores.

| Detection: Fish | Detection: Other Fish | Detection: Jellyfish |
| :---: | :---: | :---: |
| <img src="Images/Demo Image.png" alt="YOLOv8 Fish Detection" width="300"/> | <img src="Images/Demo 4.png" alt="YOLOv8 Starfish and Anemone Detection" width="300"/> | <img src="Images/Demo 5.png" alt="YOLOv8 Jellyfish Detection" width="300"/> |


## 💻 Setup and Training Instructions

### 1. Data Preparation: The Crucial Setup 

The success of the training relies on the dataset being correctly formatted in the YOLO structure. The notebook expects a file named **`data.zip`** which, upon extraction, must contain the following standard structure:
- images
- labels
- classes.txt

### 1. Run the Colab Notebook

The quickest way to replicate the training and inference is by following the steps in the [Colab Notebook](https://colab.research.google.com/drive/1fT69gJyAz39IrlM2o4_y7fuaZ_Knwdfl?usp=sharing).

### 2. Required Setup Steps in Colab

The notebook typically requires these initial steps:

```python
!git clone https://github.com/HZAI-ZJNU/Mamba-YOLO.git
!pip install ultralytics -q
```
### 3. Training Command
```python
!yolo detect train data=/content/data.yaml model=yolov8n.pt epochs=200 imgsz=640
```
