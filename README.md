login Process:
OpenCV:
For capturing and pre-processing face images.

TensorFlow / Keras or PyTorch:
Training and running a convolutional neural network (CNN) model for face recognition.

FaceNet / DeepFace (or custom model):
Feature extraction from captured images to compare with stored embeddings.

Initiating Face Login:
On the login page, users opt for face recognition.

Live Face Capture:
The application accesses the webcam (via WebRTC) and captures a live image of the user’s face.

Verification:
The captured image is processed to extract face embeddings, which are then compared with the stored embeddings using a similarity threshold.

Authentication Success/Failure:
If the similarity meets the predefined threshold, the user is authenticated and issued a JWT for the session. Otherwise, the login attempt fails, and the user is prompted to try again or use the traditional login method.

Quiz Participation:

Authenticated users can access the quiz dashboard, select quizzes, and view their performance after completion.
