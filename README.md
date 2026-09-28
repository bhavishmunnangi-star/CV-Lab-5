Computer Vision Lab 5 – Intensity Level Slicing
Overview

This project demonstrates Intensity Level Slicing, an image-processing technique used to highlight pixels within a specific range of intensity values.

In this experiment, a grayscale image is processed to identify pixels whose intensity values fall within a specified range. The selected pixels are highlighted in white, while the remaining pixels are either set to black or preserved from the original image.

The experiment demonstrates two types of intensity level slicing:

Intensity Level Slicing Without Background

Intensity Level Slicing With Background

Technologies Used

Python

OpenCV (cv2)

NumPy

Matplotlib

Google Colab

Input Image

The program reads the following grayscale image:

/content/space-odyssey.jpg


The image is loaded in grayscale mode:

img = cv2.imread("/content/space-odyssey.jpg", 0)

Intensity Range

The intensity range selected in this experiment is:

r_min = 100
r_max = 200


Therefore, all pixels with intensity values between 100 and 200 are selected.

100 ≤ Pixel Intensity ≤ 200

What is Intensity Level Slicing?

Intensity level slicing is a technique used to highlight a particular range of gray-level intensities in an image.

For an 8-bit grayscale image, intensity values range from:

0 → Black
255 → White


By selecting a particular intensity range, specific regions of an image can be emphasized.

For this experiment:

Pixels between 100 and 200 are highlighted with a value of 255 (white).

Other pixels are treated differently depending on the type of slicing.

Slicing Without Background

In slicing without background, pixels within the specified intensity range are highlighted, while all other pixels are set to black.

The output image is initialized with zeros:

slicing_w_o_background = np.zeros(img.shape)


For every pixel:

if r_min <= pixel_value <= r_max:
    slicing_w_o_background[i][j] = 255


Therefore:

Pixel intensity 100–200 → 255 (White)
All other pixels       → 0   (Black)


This makes the selected intensity range clearly visible against a black background.

Slicing With Background

In slicing with background, the original image is copied first:

slicing_w_background = img.copy()


Pixels within the selected range are then highlighted:

if r_min <= pixel_value <= r_max:
    slicing_w_background[i][j] = 255


In this case:

Pixel intensity 100–200 → 255 (White)
Other pixels             → Original intensity


This preserves the background while emphasizing the selected intensity range.

Comparison
Method	Selected Pixels (100–200)	Other Pixels
Without Background	White (255)	Black (0)
With Background	White (255)	Original intensity
Output

The program displays three images side by side:

Original Image

Slicing Without Background

Slicing With Background

The comparison makes it possible to observe how selecting a particular intensity range changes the appearance of the image.

How to Run
Using Google Colab

Open the notebook in Google Colab.

Upload space-odyssey.jpg to the /content/ directory.

Run the code cells.

The original and intensity-sliced images will be displayed.

Required Libraries

Install the required libraries if necessary:

pip install opencv-python numpy matplotlib

Applications

Intensity level slicing is commonly used in:

Medical image processing

Satellite image analysis

Object detection

Image segmentation

Feature extraction

Highlighting specific regions of an image

Industrial inspection

Conclusion

This experiment demonstrates intensity level slicing using a grayscale image. Pixels with intensity values between 100 and 200 are highlighted to emphasize specific regions.

The experiment also demonstrates the difference between slicing with background, where the original background is preserved, and slicing without background, where all non-selected pixels are suppressed.
