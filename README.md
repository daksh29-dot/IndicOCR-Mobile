## 🔒 Model & Data Notice

This repository demonstrates the deployment and mobile-inference pipeline for an
Indic OCR system using a Vision Transformer (ViT) with CTC-based recognition.

The repository contains the Android application, preprocessing pipeline, ONNX
integration, inference utilities, and model-conversion/deployment scripts.

The original trained model weights, training dataset, and any proprietary
training/configuration details are not included in this repository due to
confidentiality and usage restrictions.

The model interface and deployment code are provided for reproducibility of the
software pipeline without disclosing restricted model assets.# IndicOCR Mobile

An offline-first Android OCR application for recognizing Indic/Odia text using an on-device Vision Transformer + CTC OCR pipeline.

## Overview

IndicOCR Mobile brings OCR inference directly to Android, allowing text recognition without requiring a constant internet connection.

The application integrates a trained OCR model using ONNX Runtime Mobile and provides an Android interface for capturing, selecting, cropping, and processing document images.

## Features

- 📱 Native Android OCR application
- 🔤 Indic/Odia text recognition
- 🧠 On-device Vision Transformer + CTC OCR inference
- ⚡ ONNX Runtime Mobile deployment
- 📷 Image capture and document selection
- ✂️ Image cropping and preprocessing
- 📴 Offline-first inference
- 🚀 ARM64 and ARMv7 support
- 🔌 Optional server-assisted OCR pipeline

## Architecture

Image
  │
  ▼
Image Selection / Camera
  │
  ▼
Cropping & Preprocessing
  │
  ▼
Text Segmentation
  │
  ▼
Vision Transformer + CTC
  │
  ▼
OCR Decoding
  │
  ▼
Recognized Indic/Odia Text


## Technology Stack

- **Android**
- **Java**
- **ONNX Runtime Mobile**
- **Vision Transformer (ViT)**
- **CTC-based OCR**
- **TextBPN** for text segmentation
- **UCrop** for image cropping
- **Offline AI inference**

## Model

The application uses a trained Vision Transformer + CTC OCR model exported to ONNX for mobile inference.

The complete model training, preprocessing, evaluation, and export pipeline is maintained separately:

👉 **[IndicOCR Model & Training Pipeline](https://github.com/daksh29-dot/IndicOCR-Model.git)**

## Project Structure

IndicOCR-Mobile/
│
├── android/
│   └── app/
│       ├── src/
│       └── ...
│
├── gradle/
├── build.gradle
├── settings.gradle
└── README.md


## Running the Application

### Requirements

- Android Studio
- Android SDK
- Android device or emulator
- Android SDK 26 or higher


Open the project in Android Studio, allow Gradle dependencies to sync, and run the application on a compatible Android device.

## AI Pipeline

The mobile application is designed around an edge-AI pipeline:

Input Image
     ↓
Preprocessing
     ↓
Text Segmentation
     ↓
ViT Feature Extraction
     ↓
CTC Sequence Prediction
     ↓
CTC Decoding
     ↓
Indic/Odia Text
    text

## Key Engineering Goals

- Low-latency on-device inference
- Reduced dependency on cloud connectivity
- Mobile-friendly model deployment
- Efficient OCR inference
- Support for Indic language documents

## Related Repository

For model training, evaluation, preprocessing, ONNX conversion, and AI pipeline implementation:

👉 **[IndicOCR-Model](https://github.com/daksh29-dot/IndicOCR-Model)**

## License

This project is intended for educational and research purposes.
