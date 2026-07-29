# 🤟 Real-Time Sign Language Recognition

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv)](https://opencv.org/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

A computer vision and deep learning system that recognizes American Sign Language (ASL) hand gestures in real time using a webcam feed, OpenCV for image processing, and a Convolutional Neural Network (CNN) for classification.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Training](#training)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Overview

This project captures live video from a webcam, isolates a Region of Interest (ROI) corresponding to the user's hand, and feeds the processed frame into a trained CNN model to classify the gesture as a specific sign language letter or symbol. It is designed as an accessible, end-to-end example of applying deep learning to real-time human–computer interaction.

## Features

- 🎥 **Real-time detection** — live webcam capture and inference with minimal latency
- ✋ **ROI extraction** — isolates the hand region from the background for cleaner input
- 🧠 **CNN-based classification** — a convolutional network trained for gesture recognition
- ⚡ **Lightweight inference** — optimized for smooth performance on consumer hardware
- 📊 **Pretrained on Sign Language MNIST** — a well-established benchmark dataset
- 💻 **Simple local setup** — minimal configuration required to run

## Demo

> Add a screenshot or GIF of the application in action.

```
images/demo.gif
```

## Tech Stack

| Category         | Tools                          |
|-------------------|---------------------------------|
| Language           | Python 3.x                      |
| Deep Learning      | TensorFlow, Keras, PyTorch      |
| Computer Vision    | OpenCV                          |
| Numerical Computing| NumPy                           |
| Model Training     | Google Colab                    |

## Project Structure

```
Sign-Language-Recognition/
│
├── Dataset/                     # Training and test data
├── Models/                      # Saved/trained model weights
├── ROIinOpenCV.py               # Real-time ROI extraction and inference script
├── sign_language_pytorch.ipynb  # PyTorch training notebook
├── requirements.txt             # Python dependencies
├── README.md
└── LICENSE
```

## Dataset

This project uses the **[Sign Language MNIST](https://www.kaggle.com/datasets/datamunge/sign-language-mnist)** dataset, a drop-in replacement for the classic MNIST dataset consisting of labeled grayscale images of ASL hand signs.

## Getting Started

### Prerequisites

- Python 3.8 or later
- A working webcam
- pip (Python package manager)

### Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Sign-Language-Recognition.git
cd Sign-Language-Recognition
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### Usage

Run real-time recognition:

```bash
python ROIinOpenCV.py
```

Position your hand within the on-screen ROI box; the predicted sign will be displayed on the video feed.

## Training

The CNN model is trained on the Sign Language MNIST dataset. A PyTorch-based training pipeline is provided in:

```
sign_language_pytorch.ipynb
```

Open the notebook in Google Colab or a local Jupyter environment to retrain or fine-tune the model on custom data.

## Roadmap

- [ ] Expand gesture vocabulary beyond the MNIST alphabet subset
- [ ] Add support for dynamic (multi-frame) gestures
- [ ] Package as a standalone desktop application
- [ ] Add unit tests and CI pipeline

## Contributing

Contributions are welcome and appreciated.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## License

This project is licensed under the [Apache 2.0 License](LICENSE).

## Acknowledgements

- [Sign Language MNIST dataset](https://www.kaggle.com/datasets/datamunge/sign-language-mnist) on Kaggle
- Original concept and blog reference: [arshad-kazi.com](http://arshad-kazi.com/sign-language-recognition-using-cnn-and-opencv/)

---

If you find this project useful, please consider giving it a ⭐ on GitHub — it helps others discover it.
