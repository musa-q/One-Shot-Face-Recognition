# Face recognition
My dissertation is the development of a smart doorbell for the visually impaired. This system uses machine learning on an embedded device to recognise people at the doorstep and audibly imform the homeowner if the person at the door is known or not. This repository is an example of a single method used for the facial recognition in the system - I have also implemented other methods, such as training both an Anomaly Detector and a Multi-Class Classifier on the known faces.

The method used for face recognition used can be described as a One-Shot method. This recognition is able to work with a single image of a person. The Jupyter Notebook (`face_detection.ipynb`) uses an image of David Blaine (in `./train`). The `dlib.get_frontal_face_detector()` is used to detect the face in the image and crop the image to the face. This face is passed into the model and an embedding is calculated. This embedding is able to be compared to embeddings of faces of other people using a Cosine similarity.

The Jupyter Notebook uses the VGGFace model to recognise faces in a set of images (in `./test`). The VGGFace model is a pre-trained CNN designed for face recognition. It is capable of identifying faces with a high degree of accuracy, even in challenging environments. The first step of face recognition is detection. To do this, Dlib's HoG face detection is used.


## Installation
The following packages are required to run this script:

- keras_vggface
- keras
- numpy
- scipy
- matplotlib
- cv2
- dlib


You can install them using pip as follows:

`pip install keras_vggface keras numpy scipy matplotlib opencv-python dlib`
