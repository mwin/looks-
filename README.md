# Data Science Image Processing 
# Wound‑Cam: Data‑Science Image‑Processing Project  
Real‑Time Wound Segmentation & Measurement with YOLO v8 and AWS IoT Core
-------------------------------------------------------------------------------

## Introduction
Chronic wounds (diabetic ulcers, pressure injuries, post‑surgical sites) require precise, frequent measurement to ensure timely intervention. Manual rulers introduce error and consume nurse time.  
**Wound‑Cam** leverages smartphone macro photography, lightweight deep‑learning segmentation, and a secure cloud pipeline to:

* capture a close‑up image,
* automatically delineate the wound boundary,
* calculate surface area (and optional depth), and
* push structured data to an IoT analytics stack for longitudinal tracking.

The goal is an **under‑\$30 point‑of‑care kit** that any home‑health nurse or field medic can deploy in seconds.

---

## Project Objectives
1. **Develop** an end‑to‑end image‑processing pipeline that runs *on‑device* (TensorFlow Lite) for offline resilience.  
2. **Compare** baseline YOLO v8‑seg with alternative lightweight models (e.g., Mobile‑SAM, Fast‑SAM) for boundary accuracy and FPS.  
3. **Integrate** AWS IoT Core to transmit JSON metrics and JPEGs to S3 with a single publish for real‑time dashboards.  
4. **Optimize** the model for ≤ 3 MB on‑disk size while maintaining ≥ 0.80 IoU on validation wounds.  

---

## Technologies & Libraries
| Layer | Stack |
|-------|-------|
| **Language** | Python 3.11 |
| **Deep Learning** | Ultralytics YOLO v8, TensorFlow Lite, PyTorch (training) |
| **Image Processing** | OpenCV‑Python, Pillow |
| **Data & Math** | NumPy, pandas |
| **Visualization** | Matplotlib, Seaborn, Streamlit |
| **Cloud / IoT** | AWS IoT Device SDK v2, AWS IoT Core, Amazon S3, AWS Lambda (optional) |

---

## Getting Started

### 1. Prerequisites
* **Python 3.9+** – [Download](https://www.python.org/downloads/)  
* An **AWS account** with IoT Core enabled  
* The following Python libraries (see *requirements.txt*)

```bash
pip install -r requirements.txt




