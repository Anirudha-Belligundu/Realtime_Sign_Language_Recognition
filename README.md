# Real-Time Image Classification Using TensorFlow and OpenCV

This project demonstrates a basic real-time image classification system using a pre-trained TensorFlow Keras model, OpenCV for webcam access, and the CVZone wrapper to simplify certain computer vision tasks. It is meant as a lightweight prototype for alphabet recognition and currently supports recognition of only three characters: **A**, **B**, and **C**.

## Project Description

The goal of this project is to recognize hand signs or visual inputs corresponding to the first three letters of the English alphabet. A user places their hand or an object in front of the webcam, and the model predicts whether the visual corresponds to **A**, **B**, or **C**.

The workflow involves:

- Capturing real-time video frames using OpenCV.
- Preprocessing each frame to match the input shape of the Keras model.
- Feeding the frame into the model and reading predictions.
- Displaying the predicted label and confidence score live on the video feed using CVZone utilities.

## Model Details

The model used (`keras_model.h5`) is a basic image classifier trained to differentiate among the three classes: **A**, **B**, and **C**. The label mapping is stored in `labels.txt`, with each line corresponding to one class index in the same order as the model's softmax outputs.

The model is lightweight and designed for demonstration purposes. It can be easily replaced with a more advanced model trained on a larger dataset.


## Running the Project

1. Ensure the following files are placed inside a folder named `Model` (case-sensitive):
    - `keras_model.h5`
    - `labels.txt`

2. Launch the main script using:

```
python test.py
```

If the webcam does not activate:
- Check if it's used by another program.
- Try changing the webcam index (`cv2.VideoCapture(0)` → `cv2.VideoCapture(1)` or `2`).


## Current Status

- Model inference works for 3 classes: **A**, **B**, **C**
- Webcam integration functional
- Real-time prediction and overlay
- Extended class support (To be implemented)
- GUI or desktop interface (Future scope)

