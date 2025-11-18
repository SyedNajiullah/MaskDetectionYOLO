# 😷 YOLOv8 Mask & No-Mask Detection

## 🚀 Project Overview

This repository hosts a real-time object detection model trained using **Ultralytics YOLOv8** for the task of identifying whether individuals are wearing a **mask** or a **no-mask**.

The project includes the training notebook, the final model weights, and the necessary scripts for deployment.

Inorder to acces the dataset I have used use you API key in the roboflow API.

---

## ✨ Features

* **State-of-the-Art Detection:** Utilizes the high-performance YOLOv8 architecture.
* **Two-Class Detection:** Detects and classifies objects into two categories:
    * `mask`
    * `no-mask`
* **Real-Time Performance:** Optimized for fast inference on GPU (T4 used in training).
* **Pre-trained Weights:** Includes the optimized `.pt` file for immediate inference.

---

## 🛠️ Installation

### Prerequisites

* Python 3.8+
  
### Setup Steps

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/SyedNajiullah/MaskDetectionYOLO.git
    ```

2.  **Install Dependencies:**
    The core dependencies are `ultralytics` and `torch`.
    ```bash
    pip install ultralytics, roboflow
    ```
    
---

## 💻 Usage

### 1. Training and Validation (Using Notebook)

The `MaskDetetion.ipynb` Jupyter Notebook contains the complete workflow, including:

* Installation of dependencies (e.g., Roboflow).
* Dataset download and preparation.
* Model configuration.
* Training the YOLOv8 model.
* Validation and performance evaluation.

To run, simply open the notebook in a Jupyter environment (like Google Colab) and execute the cells sequentially.

### 2. Running Inference

You can run predictions on new images or video files directly using the trained weights file, `face_detection_model.pt`.

**Example Inference Command (Image):**
Replace `path/to/your/image.jpg` with your file path.

```bash
yolo predict model=face_detection_model.pt source='path/to/your/image.jpg' save=True
