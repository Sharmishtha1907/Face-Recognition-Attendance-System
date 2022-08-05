# Face-Recognition-Attendance-System
Face Recognition Attendance System for a single entry each day 
Face Recognition
PROBLEM STATEMENT:

    Face Recognition: Here I have made a Face Recognition model that tells whether a face matches any face in database or not, integrated with an automatic attendance marker. Typically, it is used in authentication of people with respect to digital images or IDs. Facial recognition systems are employed throughout the world today by governments and private companies. This type of technology is what makes it possible to monitor and track people in real time.
   
Introduction :

This project is based on the article Adam Geitgey. This project uses the pre trained model of a face recognition available as face_recognition package for python to detect, manipulate and identify faces. The libraries and tools that have been used to implement the model are:

1.	Visual Studio Code: It is a streamlined code editor with various forms of support for debugging, task running and version controlling. 
2.	Opencv: OpenCV is a Python open-source library, that is used for computer vision in Artificial intelligence, Machine Learning, face recognition, image processing etc. It supports variety of language such as Java, C++, Python, etc. 
3.	OS : It is a library that provide helpful tools for interfacing the underlying operating system that is being used to run the python code respectively. It helps with creating directories, managing paths, accessing various files and changing the environment variables.
4.	Numpy: It is a shortform for NumericalPython which is a python library. It is utilized for working with array or matrix. It consists of multidimensional- array object and collection of routines and sub routines for processing those arrayS.
5.	Face_Recognition: It is a python library built using dlib and provides accuracy over 99 percent. It is solely used for operations related to face.



More about face-recognition library  :

It was built using dlib’s state-of-the-art face recognition with deep learning. It detects, recognizes and manipulates faces.   The model has an accuracy of 99.38% on the Labeled Faces in Wild dataset.
Features:
1.	Detecting faces in pictures : It can be used to detect multiple faces in the same picture without any hustle.
2.	Manipulating facial features : It gets locations and outlines of facial features such as eyes, mouth, nose, chin , lips , ears, etc.
3.	Identifying faces in pictures : Recognize multiple faces in same image or digital segment.

Drawback:
This model is trained on adults and does not work effectively on children as it tends to mix them up using comparison threshold of 0.6.
Pre-requites:

Before proceeding with face recognition system, we are required to have knowledge about basic concepts of Artificial Intelligence and Machine Learning. A prior knowledge of programming language which can be used to implement ML, preferably python. We also need to visualize the steps required in creating and awareness of all libraries that we are going to use. We need to download certain dependencies such as Cmake, DLib, Visual Studio code for C++ patched with Cmake.
Theory: 

Face recognition technology uses machine learning and algorithms to extract human faces from large images and identify the person in it; Such images often contain many non-facial objects, such as structures, geography, and various body parts. It used optical input to analyze the image precisely the face. It is used almost in every field whether it is business or home. Face recognition is a type of pattern recognition. We identify a person based on the pattern of their facial features 
Currently face recognition is used in many apps such Facebook uses it for tagging, snapchat uses it for creating bit emojis, Google lens uses it search on various platform. Even our camera uses face recognition. Nowadays most prominent use of face recognition is unlocking a phone. Almost every Phone can b unlocked with face recognition. Face recognition is often used to apply filter,, like if you want your eyebrows to look like some artist there are various apps that can do that.




METHODOLOGY: 

This project illustrates Recognition System. In this project, we use pre-trained face recognition model to identify a person and mark its attendance along with date and time and save it in a csv file.
 
The pre-trained face_recognition model works in following steps:
1.	Detecting faces: In the pipeline, the first thing it does is to detect all the faces in the image and locate them.  It is using the Histogram of Oriented Gradients (HOG) method, invented in 2005. It converts our image to grayscale and look through every single pixel in our image one at a time. For each pixel the model analyzes the pixels that directly surrounds it. The goal is to compare the darkness of current pixels and the ones that directly surround it. It then simply draws an arrow determining the increase of darkness from pixel to another. We repeat the process till every pixel is replaced by arrow. The arrows are called gradients and can show the flow of light from dark across the entire image. We use tis method because if we directly analyze the pixels then the same person might have different pixel values. We then break up our image into smaller squares of 16*16 pixels each. It then counts all gradients in major direction and then replace with ones that are most intense. As a result, our image gets flattened and all we get is imprint of facial features.
 
2.	Posing and projecting faces: Once the faces have been isolated, we come to face a big problem that is angle of a face. For a computer the faces at two different angles would be faces of two different people even though it belongs to the same person. To overcome this, we provide landmarks to facial features and face_detection library used method proposed by Vahid Kazemi and Josephine Sullivan in 2014. In this we use 68 specific landmarks that exist on every face and compare it with our testing image.  It manipulates our image by turning the face till we get roughly similar location of mouth and eyes as that of testing image. 
         

3.	Face Encodings: The model extracts few basic measurements from each face and then compares them. The one with closest difference is selected as the identity. These few basic measurements include spacing between eyes, length of nose, shape of eyebrows and lips, etc. This process utilizes convolutional neural network. There are 128 face encodings which are embedded using machine learning.
Steps involved in face recognition and automatic attendance marker :
Calculating all the encoding in dataset: We first find all the encodings of al the images in the dataset and save it in form of a list. In addition to this we extract the name as well and store it in another list. All this work is done by operations such as face_location, find_faces, find_encodings, find distance provided by  the face_recognition python library.

 
Comparing the encodings with testing images: We then use our web cam to give live feed, we convert each frame to image and find encodings then we compare it with the ones in dataset. We save the index number of the encoding in dataset with least difference and use it to extract name. If the person is identified, we make rectangular box around it and display the name. In case the difference of encodings is more than 0.2 we mark the person as unidentified and display nothing.
 
Results: 

Marking Attendance: Once the person is identified, we add the name to the csv file along with date and time. 
Limitations of model:
The accuracy of the model is high but depends solely on the quality of the images such as clarity, orientation, light exposure, size, etc. In worst case scenario the model fails to identify the person correctly. One more drawback of this model is that it cannot work on large dataset. I tried using it on LWF dataset containing 19000 identities, but it was taking more than 45 minutes to find all encodings and save it in a list. 

APPLICATION OF ANPR:
1.	Security and Defense
2.	Hospitality 
3.	HealthCare  
4.	Verification 
5.	Attendance
6.	Authentication
7.	Biometrics

CONCLUSION:
This project has successfully implemented AI to identify a person. The completion of the project went quiet well, I learned much new things while I was building up it, and I get up to know various platforms which help us to learn all this stuff. I was able to learn the practical use of Python as a powerful language and it’s Open CV library. The practical helped me to learn the debugging of Python code and use of Google Colab.
Overall working on this project was great fun as I came up with great piece of knowledge and understanding of the topic.

REFERENCE:
•	Stack Overflow
•	Youtube
•	Google
•	Wikipedia


