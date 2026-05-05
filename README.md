# mini-project
detects Age and gender by using openCV
# Age and Gender Detection using OpenCV

## Overview

This project implements a **real-time Age and Gender Detection system** using **OpenCV Deep Neural Networks (DNN)**. The program detects faces from an image or webcam stream and predicts the **age range and gender** of each detected person.

The system uses pre-trained deep learning models for **face detection, age classification, and gender classification**.

---

## Features

* Detects faces in real time using a deep learning face detector.
* Predicts **gender (Male / Female)**.
* Predicts **age range** from predefined categories.
* Works with:

  * Webcam input
  * Image input
* Displays predictions directly on the video/image frame.

---

## Technologies Used

* Python
* OpenCV
* Deep Learning (DNN module)
* Caffe Models

---

## Model Files Used

The project requires the following pretrained models:

### Face Detection

* `opencv_face_detector.pb`
* `opencv_face_detector.pbtxt`

### Age Detection

* `age_net.caffemodel`
* `age_deploy.prototxt`

### Gender Detection

* `gender_net.caffemodel`
* `gender_deploy.prototxt`

---

## Age Categories

The model predicts age in the following ranges:

```
(0-2)
(4-6)
(8-12)
(15-20)
(25-32)
(38-43)
(48-53)
(60-100)
```

---

## Gender Categories

```
Male
Female
```

---

## Installation

### 1. Clone the Repository

```
git clone https://github.com/siddhik-reddy/Age-and-Gender-Detection.git
cd Age-and-Gender-Detection
```

### 2. Install Dependencies

```
pip install opencv-python
```

---

## How to Run

### Run with Webcam

```
python detect.py
```

### Run with an Image

```
python detect.py --image image.jpg
```

---

## How It Works

1. The program captures frames from a webcam or image.
2. The **face detection model** identifies faces in the frame.
3. Each detected face is cropped and processed.
4. The cropped face is passed into:

   * **Gender classification model**
   * **Age classification model**
5. Predictions are displayed on the image/video frame.

---

## Output

The program displays:

* Bounding box around detected faces
* Predicted **gender**
* Predicted **age range**

Example output:

```
Gender: Male
Age: 25-32 years
```

---

## Example

Output window showing:

```
Male, (25-32)
Female, (15-20)
```

with bounding boxes around detected faces.

---

## Future Improvements

* Improve prediction accuracy using larger datasets
* Add emotion detection
* Deploy as a web application
* Integrate with surveillance or attendance systems

---

## Author

**praveen k**

---

## License

This project is free to use for educational and research purposes.
