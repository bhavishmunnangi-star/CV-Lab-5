# Edge Detection Using Sobel, Prewitt and Canny

## 1. Introduction

This project demonstrates edge detection in digital images using three popular techniques:

* Sobel Edge Detection
* Prewitt Edge Detection
* Canny Edge Detection

The input image is converted into grayscale, and each edge detection technique is applied. The results are displayed together for comparison.

## 2. Objective

* To detect edges in a grayscale image.
* To implement Sobel, Prewitt, and Canny edge detection.
* To compare the results produced by different edge detection techniques.
* To understand the importance of edge detection in image processing.

## 3. Requirements

### Software

* Python 3.x
* OpenCV
* NumPy
* Matplotlib
* Google Colab or Jupyter Notebook

### Installation

Install the required libraries using:

```bash
pip install opencv-python numpy matplotlib
```

For Google Colab:

```python
!pip install opencv-python numpy matplotlib
```

## 4. Methodology

### Step 1: Read Image

The input image is loaded using OpenCV and converted to grayscale.

### Step 2: Sobel Edge Detection

The Sobel operator calculates the intensity changes in the horizontal and vertical directions and combines them to detect edges.

### Step 3: Prewitt Edge Detection

The Prewitt operator uses horizontal and vertical kernels to detect edges in different directions.

### Step 4: Canny Edge Detection

The Canny method detects edges using multiple stages, including gradient calculation, non-maximum suppression, and thresholding.

### Step 5: Comparison

The original grayscale image and the three edge-detected images are displayed using Matplotlib.

## 5. Output

The program displays four images:

1. Original Grayscale Image
2. Sobel Edge Detection
3. Prewitt Edge Detection
4. Canny Edge Detection

## 6. Result

The project successfully detects edges using Sobel, Prewitt, and Canny operators. The three techniques produce different edge maps, allowing their performance to be compared.

## 7. Applications

* Image segmentation
* Object detection
* Shape recognition
* Computer vision
* Feature extraction
* Medical image processing

## 8. Conclusion

Edge detection is an important technique in image processing and computer vision. Sobel, Prewitt, and Canny operators can effectively identify boundaries and important features in images. Among these methods, Canny generally produces thin and well-defined edges.

## 9. Author

**Project: Edge Detection Using Sobel, Prewitt and Canny**
