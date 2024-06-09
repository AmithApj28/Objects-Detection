# Objects-Detection

Overview
This project is a Flask web application that allows users to upload images, processes these images to detect contours, and then returns the processed images with detected contours highlighted. The application also provides the count of detected objects.

Features
1.Welcome Page: A landing page served at the root URL (/), delivering the welcome.html file.
2.Main Page: An additional page served at /main, delivering the index.html file.
3.Image Upload and Processing:
Users can upload images via a POST request to /upload.
The application processes the uploaded image to detect contours and returns the processed image along with the original.
Provides a JSON response containing:
URLs to the original and processed images.
The count of detected objects.

Image Processing Steps
1.Upload and Save:
The uploaded image is saved in a designated folder (uploads).

2.Reading and Conversion:
The saved image is read using OpenCV.
Converted to grayscale.

3.Blurring:
Gaussian Blur is applied to reduce noise.

4.Edge Detection:
Canny edge detection is used to identify edges in the image.

5.Contour Detection:
The edges are dilated to close gaps.
Contours are detected from the dilated edges.

6.Drawing Contours:
Contours are drawn on the original image.
The processed image with contours is saved.

Software Requirements
1.Python: Version 3.6 or higher is recommended.
2.pip: Python package installer.

Python Packages:
You need to install the following Python packages:
Flask: A lightweight WSGI web application framework.
OpenCV: A library for computer vision tasks (specifically, opencv-python-headless if you don't need GUI features).

Project Directory Structure:
1.app.py: Your main Flask application file.
2.uploads/: Directory for storing uploaded and processed images.
3.welcome.html: HTML file for the welcome page.
4.index.html: HTML file for the main page, including a form to upload images.
