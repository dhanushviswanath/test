Argus - Multimodal Drone Detection System

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-important)](https://www.docker.com/)
[![YOLOv8](https://img.shields.io/badge/YOLOv8-Detection-success)](https://ultralytics.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Argus is an end-to-end proof-of-concept system that fuses data from video, RF, acoustic, and radar sensors to automatically detect and track unmanned aerial vehicles (UAVs). Named after the all-seeing giant of Greek mythology, this project demonstrates modern data engineering, machine learning, and DevOps practices in a unified pipeline.

🚀 Features

* Multi-Sensor Ingestion: Processes data from video streams, RF signals (ADS-B), acoustic recordings, and simulated radar.
* AI-Powered Detection: Utilizes fine-tuned YOLOv8 models for visual detection and Scikit-learn models for audio classification.
* Sensor Fusion: Implements a central fusion engine to correlate detections across modalities for higher confidence alerts.
* Modern Data Stack: Built with TimescaleDB (time-series data), MinIO (object storage), and Docker for a reproducible environment.
* Live Dashboard: Features a Streamlit-based dashboard for real-time visualization of tracks, alerts, and sensor data.

🛠️ Tech Stack

* Languages: Python
* ML Framework: PyTorch, Ultralytics YOLOv8, Scikit-learn, Librosa
* Databases: PostgreSQL/TimescaleDB, MinIO (S3-compatible)
* Infrastructure: Docker, Docker Compose
* Dashboard: Streamlit, Grafana

📁 Project Structure
Argus/
├── data/ # SYMLINK to external drive (Not version-controlled)
├── models/ # Trained model weights
├── src/ # Source code
│ ├── ingestion/ # Data download & simulation scripts
│ ├── processing/ # Core AI and fusion logic
│ ├── database/ # DB initialization and clients
│ ├── alerting/ # Alert generation logic
│ └── dashboard/ # Web dashboard code
├── config/ # Configuration files (YAML)
├── tests/ # Unit and integration tests
├── docs/ # Project documentation
├── docker-compose.yml # Defines all services
└── requirements.txt # Python dependencies



 🚦 Getting Started

# Prerequisites

*   `git`
*   `Python 3.10+`
*   `Docker` & `Docker Compose`

💻Installation & Setup

1.  Clone the repository:
    ```bash
    git clone https://github.com/<your-username>/Argus.git
    cd Argus
    ```

2.  Set up Python environment and install dependencies:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3.  Start the backend infrastructure:
    ```bash
    docker-compose up -d
    ```
    This command will start:
    *   TimescaleDB on port `5432`
    *   MinIO on port `9000`
    *   Grafana on port `3000`

4.  Initialize the database:
    ```bash
    python src/database/init_db.py
    ```

(More detailed instructions for data acquisition and model training will be added as the project develops.)

 📊 Status

Current Phase: Phase 1 - Data Acquisition & Environment Setup
- [X] Project Repository Initialized
- [ ] OpenSky RF Data Ingestion Script
- [ ] Anti-UAV Video Data Download
- [ ] Radar Data Simulator
- [ ] Docker Compose Infrastructure Running

 👨‍💻 Developer

Your Name
*   Masters in IT Management, University of Wisconsin Milwaukee
*   Bachelors in Mechatronics, Mahatma Gandhi Institute of Technology
*   [LinkedIn](https://www.linkedin.com/in/your-profile/) | [GitHub](https://github.com/your-username)

 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
