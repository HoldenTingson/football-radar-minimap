# Computer Vision Project: Football Radar Minimap

## Background
![11](https://github.com/user-attachments/assets/fb614125-2312-419d-9144-a55c800597eb)

In modern football, tactical analysis has become a crucial determinant of team success. However, conventional camera angles have limitations in capturing accurate spatial information about player positions and movements, making it challenging for coaches and analysts to analyze tactical patterns effectively.

## Objectives
1. Object Detection: Detect and classify objects (ball, players, referees) on the football pitch.
2. Transformation: Converts object coordinates from camera perspective into a 2D field view (bird's eye view).
3. Minimap Overlay: Display a tactical minimap that shows the position and movement of the players, referees, and ball objects.

## Datasets
| Dataset | Purpose | Source |
|---------|---------|--------|
| [![Download Dataset](https://app.roboflow.com/images/download-dataset-badge.svg)](https://universe.roboflow.com/roboflow-jvuqo/football-players-detection-3zvbc) | Football Player Detection | Roboflow Universe |
| [![Download Dataset](https://app.roboflow.com/images/download-dataset-badge.svg)](https://universe.roboflow.com/roboflow-jvuqo/football-field-detection-f07vi) | Pitch Keypoint Detection | Roboflow Universe |
| [![DFL - Bundesliga Data Shootout](https://img.shields.io/badge/Download-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/competitions/dfl-bundesliga-data-shootout) | Football Match Footage | Deutsche Fußball Liga e.V. |

## Models
* YOLOv8 (Player Detection) - Detects players, referees, and the ball in the video.
* YOLOv8 (Pitch Detection) - Identifies the football pitch boundaries and key points.
* SigLIP - Extracts features from image crops of players.
* UMAP - Reduces the dimensionality of the extracted features for easier clustering.
* KMeans - Clusters the reduced-dimension features to classify players into two teams.

## System Implementation
### Model Training Phase
1. **Train football player detection model**
   - Dataset preparation and annotation
   - YOLOv8 model training for players, referees, and ball detection
   
2. **Train pitch keypoint detection model**
   - Field boundary annotation
   - YOLOv8 model training for pitch keypoint detection

### Inference Phase
1. **Object detection**
   - Detect players, referees, and ball using trained football player detection model
   - Extract bounding boxes and confidence scores

2. **Team classification**
   - Extract player image crops from detections
   - Apply SigLIP feature extraction
   - Use UMAP for dimensionality reduction
   - Classify teams into home and away using K-means clustering

3. **Field analysis**
   - Detect pitch keypoints using trained pitch keypoint detection model
   - Identify field boundaries and reference points

4. **Output generation**
   - Project pitch lines on output frame
   - Overlay player positions with team color coding
   - Display referees and ball tracking

## System Overview
### Input Video

https://github.com/user-attachments/assets/7f9543a0-81e7-4c9a-b0e1-1c624b0bc4d4

### Output Video

https://github.com/user-attachments/assets/c81f7aa3-d4cc-45a5-973e-1cf5cef3c9f4

## UI Display

![ui_display](https://github.com/user-attachments/assets/1f09ab5d-40b1-47d5-bcaa-a68f5e714e7e)
