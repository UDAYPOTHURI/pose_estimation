# Pose Estimation and Angle Calculation using MediaPipe

This project demonstrates real-time pose estimation and angle calculation using MediaPipe and OpenCV. It captures video from a webcam, detects body landmarks, calculates joint angles, and displays posture warnings based on these angles.

## Project Structure

- `pose_estimation_angle_calculation.py`: Python script that performs pose estimation, calculates joint angles, and displays results and warnings.
- `README.md`: Documentation for the project.

## Dependencies

Ensure you have the following Python packages installed:

- `opencv-python`
- `mediapipe`
- `numpy`

## Code Overview

### Functions

- `calculate_angle(a, b, c)`: Calculates the angle between three points `a`, `b`, and `c`. Returns the angle in degrees.

- `check_posture_warnings(angles)`: Checks the calculated angles against predefined thresholds and returns a list of warnings if any angles indicate poor posture.

### Main Script

1. **Initialization:**

   Sets up MediaPipe Pose solution and OpenCV video capture.

2. **Pose Detection:**

   Captures video frames, converts them to RGB, and processes them with MediaPipe Pose to get landmarks.

3. **Angle Calculation:**

   Calculates angles for various joints using the `calculate_angle` function.

4. **Posture Warnings:**

   Uses the `check_posture_warnings` function to generate warnings based on the calculated angles.

5. **Visualization:**

   Displays calculated angles and warnings on the video feed and draws landmarks and connections using OpenCV.

## Posture Warning Thresholds

- **Shoulder Angles:** Warns if the angle is greater than 160 degrees.
- **Hip Angles:** Warns if the angle is outside the range of ±30 degrees.
- **Knee Angles:** Warns if the angle is greater than 160 degrees.
- **Ankle Angles:** Warns if the angle is outside the range of ±30 degrees.
