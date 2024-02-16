# Line Tracking Algorithm for Parrot Mini Drone


This repository features an algorithm for the Parrot mini drone, designed for autonomously following a colored line, ending in a landing circle. Developed in Simulink MATLAB, it uses the drone's camera for line detection and computes controls to maintain the flight path.

Algorithm Highlights
The algorithm consists of two main components:

1.Line Recognition and Direction Determination: It processes camera images to detect edges (Canny filter) and applies the Hough transform for line extraction. The algorithm averages coordinates of the two main lines, providing a central path for direction guidance. Challenges in direction accuracy, especially at turns, are addressed with additional methods.

2.Bitmap-Based Direction Correction: This method uses bitmap images of the line. Triangular regions of interest (ROIs) in the image center, oriented based on previous directions, intersect with the line's bitmap to refine the heading. This enhances stability and direction consistency.

The algorithm includes a landing feature using MATLAB's imfindcircles() function to locate the circle's center, triggering landing when aligned with the ROI.

Usage
To use this algorithm:

Set up and connect the Parrot mini drone to your computer.
Open the MATLAB project or script with the algorithm.
Configure camera and ROI settings.
Run the script or Simulink simulation.
Observe and adjust as needed for optimal performance.

Requirements
Needed for this algorithm:

-Parrot mini drone
-MATLAB with Simulink and Computer Vision Toolbox

<a href="https://youtu.be/0yPXIfl6oJo
" target="_blank"><img src="http://img.youtube.com/vi/0yPXIfl6oJo/0.jpg" 
alt="UAV Line Follower" width="240" height="180" border="10" /></a>
