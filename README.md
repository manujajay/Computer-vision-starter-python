# Computer-Vision-Starter-Python

This repository is designed to help beginners get started with computer vision projects using Python and OpenCV. It includes examples of basic image processing tasks and techniques to handle video input.

## Prerequisites

- Python 3.6 or higher
- OpenCV library

## Installation

Install Python and OpenCV with the following command:

```bash
pip install opencv-python-headless
```

## Basic Usage Examples

### 1. Reading and displaying an image

```python
import cv2

# Load an image
image = cv2.imread('input.jpg')

# Display the image
cv2.imshow('Image', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### 2. Convert an image to grayscale

```python
import cv2

# Load an image
image = cv2.imread('input.jpg')

# Convert to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Display the grayscale image
cv2.imshow('Grayscale Image', gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### 3. Basic video processing

```python
import cv2

# Capture video from the first camera connected to your computer
cap = cv2.VideoCapture(0)

while True:
    # Read a new frame
    ret, frame = cap.read()
    
    # Convert frame to grayscale
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
    
    # Display the resulting frame
    cv2.imshow('Frame', gray)
    
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# When everything done, release the capture
cap.release()
cv2.destroyAllWindows()
```

## Contributing

Contributions that improve the documentation, extend example code, or enhance the functionality are highly appreciated. Please fork this repository, create a feature branch, and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
