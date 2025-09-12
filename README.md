# Argus - Multimodal Drone Detection System

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-important)](https://www.docker.com/)
[![YOLOv8](https://img.shields.io/badge/YOLOv8-Detection-success)](https://ultralytics.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Argus is an end-to-end proof-of-concept system that fuses data from video, RF, acoustic, and radar sensors to automatically detect and track unmanned aerial vehicles (UAVs). Named after the all-seeing giant of Greek mythology, this project demonstrates modern data engineering, machine learning, and DevOps practices in a unified pipeline.

## 🚀 Features

* Multi-Sensor Ingestion: Processes data from video streams, RF signals (ADS-B), acoustic recordings, and simulated radar.
* AI-Powered Detection: Utilizes fine-tuned YOLOv8 models for visual detection and Scikit-learn models for audio classification.
* Sensor Fusion: Implements a central fusion engine to correlate detections across modalities for higher confidence alerts.
* Modern Data Stack: Built with TimescaleDB (time-series data), MinIO (object storage), and Docker for a reproducible environment.
* Live Dashboard: Features a Streamlit-based dashboard for real-time visualization of tracks, alerts, and sensor data.

## 🛠️ Tech Stack

* Languages: Python
* ML Framework: PyTorch, Ultralytics YOLOv8, Scikit-learn, Librosa
* Databases: PostgreSQL/TimescaleDB, MinIO (S3-compatible)
* Infrastructure: Docker, Docker Compose
* Dashboard: Streamlit, Grafana

## 📁 Project Structure
