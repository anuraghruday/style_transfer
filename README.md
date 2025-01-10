# README

## Project Overview

This project combines neural style transfer with emotion detection to explore how visual stimuli (specifically, artwork) can influence human emotions. The goal is to use a webcam to capture a user's facial expression, analyze the emotion, apply style transfer to the image, and then capture a new image of the user to detect any changes in their emotional state.

## Prerequisites

To run this project, you'll need the following dependencies:

- Python 3.x
- TensorFlow 2.x
- PyTorch 1.x
- OpenCV
- NumPy
- Matplotlib
- Pillow

You can install the required packages using the following command:

```bash
pip install tensorflow torch opencv-python-headless numpy matplotlib pillow

```

### How It Works

1. Capture Initial Image: The webcam captures an image of the user's face.
2. Emotion Detection: The captured image is processed using a pre-trained ResNet-18 model modified for grayscale emotion detection. The model predicts the user's current emotion.
3. Neural Style Transfer: The project uses a pre-trained VGG19 model to apply a style transfer to the captured image, blending it with the style of the famous artwork "Starry Night."
4. Capture Reaction Image: After displaying the stylized image, the webcam captures another image of the user's face to analyze any changes in emotion.
5. Compare Emotions: The initial and final emotions are compared to determine if the style transfer influenced the user's emotional state.


### Files

- emotion_model_15.pth: Pre-trained PyTorch model for emotion detection.
- Starry-Night.png: Style image used for style transfer.
- captured_image.jpg: Image captured from the webcam before style transfer.
- best_generated_image.npy: The best-stylized image was generated during training.
- captured_image_2.jpg: Image captured from the webcam after style transfer.


### Running the code

- clone the repository and navigate to the project directory
- Run the run.ipynb file

### The script will:

- Capture an image from your webcam.
- Predict the initial emotion and display it.
- Apply style transfer to the captured image.
- Capture another image after displaying the stylized image.
- Predict and display the new emotion, along with the target emotion.

### Emotion Classes

The emotion detection model recognizes the following emotions:

- Angry
- Disgust
- Fear
- Happy
- Sad
- Surprise
- Neutral


You can adjust parameters such as epochs, patience, and learning_rate to experiment with different training configurations.
