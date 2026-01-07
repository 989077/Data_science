This project is a real-time computer vision application built using OpenCV. It captures video from your webcam to detect faces, eyes, and smiles simultaneously,
applying bounding boxes and text labels to the live stream.

Smart Face Detector
A Python-based facial feature detection system that utilizes Haar Cascade Classifiers to identify multiple human attributes in real-time.

Features-
 -- Real-time Face Detection: Identifies faces and outlines them with bounding boxes.

 -- Nested Detection: Specifically looks for eyes and smiles inside the detected face region (Region of Interest - ROI) to improve accuracy and performance.

 -- Live Annotations: Overlays text alerts when specific features are identified.

 -- Optimized Performance: Uses grayscale conversion to reduce computational load during detection.

 🛠️ Prerequisites --
Before running the script, ensure you have the following installed:

 -- Python 3.x

 -- OpenCV library (opencv-python)

  -- You will also need the Haar Cascade XML files provided by OpenCV. Download them and place them in the same directory as your script:

  -- haarcascade_frontalface_alt.xml

  -- haarcascade_eye.xml

  -- haarcascade_smile.xml

🔍 How it Works -- 
1 > The application follows a structured image processing pipeline:

2 > Frame Capture: Captures a frame from the primary camera (cv2.VideoCapture(0)).

3 > Preprocessing: Converts the frame to grayscale. This is necessary because Haar Cascades operate on intensity gradients rather than color data.

4 > Face Detection: The face_cascade scans the entire image.

5 > ROI Extraction: Once a face is found, the code creates a "Region of Interest" (ROI). It only looks for eyes and smiles inside this specific box, which prevents false positives (like detecting a "smile" on a shirt pattern).

6 > Overlay: Draws rectangles and text labels using cv2.rectangle and cv2.putText.
