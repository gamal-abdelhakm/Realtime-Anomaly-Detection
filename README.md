# Realtime Anomaly Detection

A real-time smart surveillance system that aids the observer by detecting anomalies and more.

## Table of Contents

- [Description](#description)
- [Demo](#demo)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [I3D Feature Extraction](#i3d-feature-extraction)
- [Contributing](#contributing)
- [Contact](#contact)

## Description

Realtime Anomaly Detection is a smart surveillance system designed to assist observers by detecting anomalies in real-time. This system leverages cutting-edge machine learning techniques to monitor and analyze video feeds, identifying unusual activities that may require attention.

This thesis presents the development and implementation of a real-time anomaly surveillance system. The system leverages advanced techniques from computer vision, machine learning, and artificial intelligence to enable proactive monitoring and detection of anomalies in various environments. Through the utilization of state-of-the-art models and algorithms, the system provides real-time analysis of multiple camera feeds, automatically detects anomalies, and triggers appropriate actions for a timely response. The system offers a user-friendly interface, customizable settings, and integration with email notifications for efficient anomaly management. Extensive experiments and evaluations demonstrate the effectiveness and practicality of the system in enhancing situational awareness and improving overall security.

## Demo
![alt text](https://github.com/Anas-Abd-ElAziz/Realtime-Anomaly-Detection/blob/main/image.png?raw=true)
You can watch a demo of the Realtime Anomaly Detection system [here](https://drive.google.com/file/d/1iL_pEhcCIWx69TGYpBz4uxNe94V6Ecni/view?usp=sharing).

## Features

- Real-time anomaly detection
- High accuracy and low latency
- Easy integration with existing surveillance systems
- Customizable detection parameters
- Detailed logging and alerting

## Installation

To get started with Realtime Anomaly Detection, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/gamal-abdelhakm/Realtime-Anomaly-Detection.git
    ```
2. Navigate to the project directory:
    ```bash
    cd Realtime-Anomaly-Detection
    ```
3. Create a virtual environment and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
4. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

To use the Realtime Anomaly Detection system, follow these steps:

1. Ensure your video feed sources are correctly configured.
2. Run the main detection script:
    ```bash
    python main.py
    ```
3. Monitor the output for detected anomalies and alerts.

## I3D Feature Extraction

This project also includes code for I3D feature extraction using a ResNet50 backbone.

### Setup

Download pretrained weights for I3D from the nonlocal repo:
```bash
wget https://dl.fbaipublicfiles.com/video-nonlocal/i3d_baseline_32x2_IN_pretrain_400k.pkl -P pretrained/
```

Convert these weights from caffe2 to pytorch:
```bash
python -m utils.convert_weights pretrained/i3d_baseline_32x2_IN_pretrain_400k.pkl pretrained/i3d_r50_kinetics.pth
```

### Parameters

```plaintext
--datasetpath:       folder of input videos (contains videos or subdirectories of videos)
--outputpath:        folder of extracted features
--frequency:         how many frames between adjacent snippet
--batch_size:        batch size for snippets
```

### Run

```bash
python main.py --datasetpath=samplevideos/ --outputpath=output
```

## Contributing

We welcome contributions to improve Realtime Anomaly Detection! To contribute:

1. Fork the repository.
2. Create a new branch:
    ```bash
    git checkout -b feature/your-feature-name
    ```
3. Make your changes.
4. Commit your changes:
    ```bash
    git commit -m 'Add some feature'
    ```
5. Push to the branch:
    ```bash
    git push origin feature/your-feature-name
    ```
6. Open a pull request.

## Contact

For questions or support, please contact Gamal Abdelhakm at gamal.ahmed.abdelhakm@gmail.com
