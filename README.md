# Multi Pose Hand Face Detection

## To run the code, please either use "Visual Studio" or "Jupyter Notebook from Anaconda Navigator".

### Thank you.

<br>

## Code Explanation:

1. **Import Libraries:** The code starts by importing the necessary libraries, including OpenCV (cv2) for image processing and MediaPipe (mediapipe) for pose, hand, and face mesh detection.

2. **Initialize MediaPipe Solutions:** Three MediaPipe solutions are initialized: `mp_pose` for pose estimation, `mp_hands` for hand tracking, and `mp_face_mesh` for face mesh detection. Each solution is configured with specific parameters like `static_image_mode`, `max_num_hands`, `min_detection_confidence`, and `min_tracking_confidence`.

3. **Capture Video:** The code captures video frames from the default camera (index 0) using OpenCV's `VideoCapture` object.

4. **Processing Loop:** Inside the processing loop (`while` loop), the code continuously reads frames from the camera.

5. **Convert to RGB:** Each frame is converted from BGR to RGB color space because MediaPipe processes RGB images.

6. **Process Pose, Hands, and Face Mesh:** The pose, hands, and face mesh models process the RGB frame using the `process` method. The results are stored in `results_pose`, `results_hands`, and `results_face_mesh`, respectively.

7. **Draw Landmarks:** If pose landmarks are detected, the code draws the landmarks on the frame using `mp_drawing.draw_landmarks` with the appropriate landmark connections.

8. **Draw Hand Landmarks:** Similarly, if hand landmarks are detected, the code draws the landmarks and connections for each hand.

9. **Draw Face Mesh Landmarks:** If face mesh landmarks are detected, the code draws the mesh using `mp_drawing.draw_landmarks`.

10. **Display Frame:** The processed frame with all landmarks drawn is displayed using OpenCV's `imshow` function.

11. **Exit Condition:** The loop continues until the user presses the ESC key. Upon pressing ESC, the loop breaks, releasing the resources and closing all windows.

12. **Release Resources:** Finally, the MediaPipe solutions are closed, the video capture is released, and all OpenCV windows are destroyed.

## Keypoints:
- Utilizes MediaPipe solutions for pose estimation, hand tracking, and face mesh detection.
- Draws landmarks and connections for pose, hands, and face mesh on the video frames.
- Real-time processing of video feed from the default camera.
- Allows the user to exit the program by pressing the ESC key.
