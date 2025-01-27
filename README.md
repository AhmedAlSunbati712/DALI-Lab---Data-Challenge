# DALI-Lab---Data-Challenge
Detecting Barnacles using OpenCV
Steps of solving the challenge:
- Preprocessing the image:
    - Before starting to tackle the problem of detecting the barnacles, we need to address the problems of noise and computational complexity appended by the use of RGB color.
    - The latter can be addressed by transforming the image to a grayscale since we are only interested in structural features (the boundaries of the barnacles).
    - The former can be addressed by implementing a gaussian filter that smoothes out noise by averaging over neighbouring pixels using a gaussian distribution.
- Detecting Barnacles:
    - We have the grayscale, smoothened out image as an input and now we want to find contours that separate the barnacles from their surroundings and from each other.
    - We use canny edge detection from OpenCV which utilizes the gradient of intensity in images to detect edges (the gradient is perpendicular to edges).
    - Then, we use these edges to find contours of constant color/intensity.
