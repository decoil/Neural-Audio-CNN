# Neural Audio CNN

A deep learning-based audio classification system using ResNet-based Convolutional Neural Networks for real-time audio analysis.

![Neural Audio CNN Interface](screenshot.png)

## Overview

Neural Audio CNN is a full-stack web application that uses deep learning to classify audio files. Based on the T3 tech stack combining Python backend and TypeScript/React frontend, it provides real-time audio classification with visual feedback.

## Tech Stack

- **Frontend**: TypeScript, Next.js, React, Tailwind CSS
- **Backend**: Python, Modal (serverless deployment), FastAPI, Pydantic
- **Deep Learning**: TensorFlow/PyTorch with ResNet-based CNN architecture
- **Monitoring**: TensorBoard for model training visualization

## Features

- Upload and analyze audio files (.wav format)
- Real-time classification with prediction probabilities
- Audio spectrogram visualization
- Waveform display
- CNN layer activation visualization
- Responsive web interface built with Tailwind CSS

## Architecture

The CNN model is based on the ResNet (Residual Network) architecture, adapted for audio classification tasks. The model processes audio spectrograms through residual blocks that help train deeper networks effectively.

## Prerequisites

- Modal account and API key (get one at [modal.com](https://modal.com))
- Node.js and npm
- Python 3.7+

## Installation

### Backend Setup (Modal)

```bash
# Clone the repository
git clone https://github.com/decoil/Neural-Audio-CNN.git
cd Neural-Audio-CNN

# Install Python dependencies
pip install -r requirements.txt

# Setup Modal (you'll need to enter your Modal API key)
modal setup

# Run the backend locally
modal run main.py

# OR deploy to Modal cloud
modal deploy main.py
```

### Frontend Setup

```bash
# Navigate to frontend directory
cd visual-audio-CNN

# Install dependencies
npm i

# Run the development server
npm run dev
```

## Usage

1. Ensure the Modal backend is running (either locally with `modal run` or deployed with `modal deploy`)
2. Start the frontend development server
3. Open http://localhost:3000 in your browser
4. Upload an audio file to see predictions and visualizations

## Model Training

Monitor training progress with TensorBoard:
```bash
tensorboard --logdir=logs
```

## API Documentation

When running with Modal, you can access the FastAPI documentation through the Modal deployment URL.

## Credits

This project is inspired by [audio-cnn](https://github.com/Andreaswt/audio-cnn).
