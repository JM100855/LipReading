# Lip Reading

This project implements a lip-reading system that predicts spoken words using video input only. It processes videos frame by frame, focuses on mouth movements, and learns how lip motion changes over time to match spoken text.

---

## Project Goal

The goal of this project is to understand how visual speech can be recognized without using audio. It focuses on building a working pipeline for video preprocessing, model training, and evaluation.

---

## Dataset

- Uses video clips of people speaking short words or phrases  
- Each sample includes:
  - A video showing lip movements
  - A text label for the spoken content
- Videos are converted into frames and cropped to the mouth region before training

---

## Data Processing

- Video frames are extracted and converted to grayscale  
- Frames are resized, normalized, and aligned with text labels  
- The pipeline is modular and can be reused for other datasets

---

## Model Used

- 3D Convolution layers to extract features from video frames  
- LSTM layers to learn changes in lip movement over time  
- Dense and Dropout layers for prediction and regularization  
- CTC loss to handle variable-length sequences without frame-level labels  

The model is trained using TensorFlow.

---

## Training and Evaluation

- Trained using the Adam optimizer  
- Learning rate scheduling used for stable training  
- Model output is compared with ground-truth text to check correctness

---

## Repository Contents

- Jupyter notebooks for experiments and training  
- Preprocessing code for video and frame handling  
- Model definition and training scripts 

This project was built to explore visual speech recognition and gain hands-on experience with video-based sequence modeling.
