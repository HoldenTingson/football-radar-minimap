# Computer Vision Project: Football Radar Minimap

## Background
In modern football, tactical analysis has become a crucial determinant of team success. However, conventional camera angles have limitations in capturing accurate spatial information about player positions and movements, making it challenging for coaches and analysts to analyze tactical patterns effectively.

## Objectives
1. Object Detection: Detect and classify objects (ball, players, referees) on the football pitch.
2. Transformation: Converts object coordinates from camera perspective into a 2D field view (bird's eye view).
3. Minimap Overlay: Display a tactical minimap that shows the position and movement of the players, referees, and ball objects.

## Datasets
| Dataset | Purpose |
|-------|---------|
| [![Download Dataset](https://app.roboflow.com/images/download-dataset-badge.svg)](https://universe.roboflow.com/roboflow-jvuqo/football-players-detection-3zvbc) | Football Player Detection |
| [![Download Dataset](https://app.roboflow.com/images/download-dataset-badge.svg)](https://universe.roboflow.com/roboflow-jvuqo/football-field-detection-f07vi) | Pitch Keypoint Detection |
| [![DFL - Bundesliga Data Shootout](https://img.shields.io/badge/Download-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/competitions/dfl-bundesliga-data-shootout) | Football Match Footage |

## Models
* YOLOv8 (Player Detection) - Detects players, referees, and the ball in the video.
* YOLOv8 (Pitch Detection) - Identifies the football pitch boundaries and key points.
* SigLIP - Extracts features from image crops of players.
* UMAP - Reduces the dimensionality of the extracted features for easier clustering.
* KMeans - Clusters the reduced-dimension features to classify players into two teams.

## System Implementation


## System Overview

