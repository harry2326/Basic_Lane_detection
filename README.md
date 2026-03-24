Explanation Video
https://drive.google.com/drive/folders/1gmGoDvOJ-CsIo6gUKX71LfIXFV2jvEOD?usp=sharing

Lane Detection using OpenCV
This project implements a basic lane detection pipeline using computer vision techniques in Python with OpenCV. It processes a video, detects lane-like lines, and overlays them on the original frames.


The algorithm performs the following steps on each frame: Convert image to grayscale, Apply Gaussian blur to reduce noise, Detect edges using Canny Edge Detection, Apply Region of Interest (ROI) masking, Detect lines using Hough Transform, Filter lines based on angle (to keep lane-like lines only), Overlay detected lanes on the original frame, Save processed output as a new video

  
Algorithm Explanation: Grayscale Conversion - Reduces computation by converting RGB image into a single channel, Gaussian Blur - Removes noise and smoothens the image, Canny Edge Detection - Detects strong edges in the image using thresholds: Low threshold: 100 High threshold: 150, Region of Interest (ROI) - Masks irrelevant areas and keeps only the road region using a polygon, Hough Line Transform - Detects line segments from edge-detected image:
    ρ (rho): 5
    θ (theta): 1°
    Threshold: 100
    Min line length: 80
    Max line gap: 200
, Angle Filtering - Only lines with angles between 25° and 40° are considered lane lines, Overlay - Detected lines are drawn and merged with the original frame.


Requirements - Install dependencies: pip install opencv-python numpy matplotlib


Usage: Place your input video (solidYellowLeft.mp4) in the project directory,
  Run the script:python lane_detection.py,
  Output: Processed video: new_video.mp4,
  Live preview window (press q to exit)

