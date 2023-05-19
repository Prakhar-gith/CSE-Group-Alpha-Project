# CSE-Group-Alpha-Project

This code is a simple implementation of a real-time face detection using OpenCV (Open Source Computer Vision Library). It utilizes a pre-trained Haar cascade classifier, specifically the "haarcascade_frontalface_default.xml" file, to detect frontal faces in a video stream captured by a camera.

The code starts by importing the necessary modules, including pathlib for handling file paths and cv2 for image and video processing. It then sets the path to the Haar cascade XML file using pathlib.Path and prints the path to the console.

Next, it initializes a cv2.CascadeClassifier object with the path to the XML file, which will be used for face detection. It also creates a cv2.VideoCapture object to capture video frames from the default camera (index 0).

The code enters a loop that continues until the user presses the "q" key. Within the loop, it reads each frame from the camera using camera.read(), converts it to grayscale using cv2.cvtColor(), and then applies the cascade classifier to detect faces using clf.detectMultiScale(). This function takes several parameters, including the grayscale frame, scaleFactor, minNeighbors, minSize, and flags, which control the sensitivity and accuracy of the face detection algorithm.

If faces are detected, the code loops through the detected faces' coordinates and draws rectangles around them using cv2.rectangle(). It uses the frame variable to draw rectangles directly on the original colored frame.

The resulting frame with the detected faces is displayed in a window named "Faces" using cv2.imshow(). The code waits for a key press for 1 millisecond using cv2.waitKey(1), and if the pressed key is "q", the loop breaks, and the program exits.

Finally, the code releases the camera resource using camera.release() and closes all windows using cv2.destroyAllWindows().

This code serves as a basic face detection example, demonstrating how to use the Haar cascade classifier and OpenCV's video capturing and processing capabilities. It can be used as a starting point for more complex face recognition or tracking systems.
