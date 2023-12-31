# Virtual Mouse using Hand Gestures

This project demonstrates how to control your computer's mouse cursor using hand gestures captured by a webcam. It uses OpenCV, MediaPipe, and PyAutoGUI libraries to recognize hand landmarks and translate them into mouse movements and clicks.

## Prerequisites

Before running this project, you need to have the following libraries and dependencies installed:

- Python 3.x
- OpenCV (`cv2`)
- MediaPipe (`mediapipe`)
- PyAutoGUI (`pyautogui`)

You can install the required packages using `pip`:

```bash
pip install opencv-python mediapipe pyautogui
```

## Usage

1. Connect a webcam to your computer.

2. Clone or download this repository to your local machine.

3. Open the project directory in your terminal.

4. Run the Python script:

```bash
python main.py
```

5. A window will appear displaying the webcam feed with hand landmarks overlaid.

6. Point your index finger (usually the second finger) to control the mouse cursor.

7. Bring your thumb close to your index finger to perform a click action.

8. To exit the program, press `Esc` or close the window.

## How it works

- The code captures video frames from the webcam using OpenCV.

- It uses the MediaPipe library to detect hand landmarks in each frame.

- The index finger is tracked to move the mouse cursor, and the thumb is used for clicking.

- The mouse cursor's movement is relative to the screen's resolution, so it scales hand movements appropriately.

- When the index finger and thumb are close enough (within 20 pixels), it simulates a mouse click action.

## Customization

You can customize the code according to your preferences:

- Adjust the `radius` in the `cv2.circle` function to change the size of the circles drawn on the screen.

- Modify the `abs(index_y - thumb_y)` threshold to control how close the thumb needs to be to the index finger to trigger a click.

- Change the sleep duration in `pyautogui.sleep` to adjust the click's duration.

## Troubleshooting

If the program is not working as expected, try the following:

- Ensure that your webcam is properly connected and functioning.

- Check if all required libraries are installed.

- Experiment with the thresholds and parameters to fine-tune hand gesture recognition.

- Make sure there is enough lighting in your environment for better hand tracking.

## Credits

- This project uses OpenCV, MediaPipe, and PyAutoGUI libraries.

- MediaPipe is developed by Google Research.


Feel free to customize and expand upon this README as needed for your project. You can include information about additional features, troubleshooting tips, or any other relevant details.
