# Dynamic-Virtual-Gesture-System

# Abstract

With new changes seen in engineering field day by day, it become quite important for society to search out specific new ways in which of interaction with computer systems and technology as its need is increasing in society everyday. Today, all device is creating the application of touch screen technology on its computer systems, that is not affordable to be employed in every applications. A particular system sort of a virtual mouse that generates  object pursuit(tracking) and Gestures which will ease us to interact, it can be an alternate technique for the typical touch screen and also the solid physical mouse. the target is to make associate Object pursuit(tracking) application that interacts with the computer system.This system proposed is a Computer Vision-based control system, that uses hand gestures that are being captured from a digital camera through associate with hand detection technique implemented using OpenCV libraries.

Our project which applies gesture recognition as a topic which comes under two computer science fields like augmented reality and human-computer interaction and we have created a virtual gesture system with the goal of elucidating human gestures through the mathematical algorithms. Users can use simple finger or hand gestures to control or interact with the system without physically touching them and also we included a voice assistance to start and end the gesture controlling system. Gesture recognition can be viewed as a way for computers to begin to recognize human body language and signs, thus stuffing the void between computing systems and humans than earliest text user interfaces or even graphical user interfaces, which still limit the majority of input to keyboard and mouse are may not be very efficient at all times.

The algorithm is focused on deep learning for detecting the gestures. Hence, the proposed system will avoid pandemic situation of COVID-19 spread by reducing the human interaction with the devices to control the system.




# System Architecture


![image](https://user-images.githubusercontent.com/79743499/185775884-1d65d1ff-b27b-4a8b-99a8-a1ac98477ab7.png)




# Module Description

We have devised a smart framework for creating a virtual interface in this paper. As the cases of covid-19 are decreasing maximum public places are opening with half or full capacity. ATMs are always open. If we install this system in the public places like ticket counters, ATMs and computerized docking facilities, the spread of germs, bacteria, and viruses can be greatly reduced. The block diagram of the developed framework is depicted
+  Hand Detection In this module, the main focus is access the webcam and allow the program to access the hand images. 
+  Gesture Detection and Recognition In this module, the accessed images are analysed and the movements and the significant gestures are noted and stored. 
+  Accessing The Database To Check Verify Gesture In this module, the recorded gestures and movements are cross-checked with the pre- programmed gestures and movements to facilitate the program functioning 
+  Desired Actions Occur In this module, the cross-checked gestures are triggered to perform the preprogramed actions like moving cursor, scrolling, clicking, double clicking, etc.. 
+  Help From Voice Assistance In this module, we create a voice assistant to facilitate and help us use the virtual interface more efficiently and safely. It can also perform many other basic functions


# Result


By using various modules, we were able to build a virtual interface system. The system’s efficiency level is enough to fully function in a public environment. Even though there is still ground for development in the voice control module, as of right it fulfills it’s responsibilities perfectly. In it’s current level, this project is fully capable of functioning in a controlled singular environment. The program captures the images, processes them, analyses them, extracts necessary information from them, and completes the pre programmed tasks satisfactorly

![image](https://user-images.githubusercontent.com/79743499/185776023-59f8982e-d30c-453e-b2ab-789c623fdc6d.png)


+ The proposed AI virtual mouse system is based on the frames that have been captured by the webcam in a laptop or PC. By using the Python computer vision library OpenCV, the video capture object is created and the web camera will start capturing video, as shown in Figure. The web camera captures and passes the frames to the AI virtual system. 
+ The AI virtual mouse system uses the webcam where each frame is captured till the termination of the program. The video frames are processed from BGR to RGB color space to find the hands in the video frame by frame as shown in the following code: def findHands(self, img, draw = True): imgRGB = cv2.cvtColor(img, cv2.COLOR_BGR2RGB) self.results = self.hands.process(imgRGB) 
+ The AI virtual mouse system makes use of the transformational algorithm, and it converts the co-ordinates of fingertip from the webcam screen to the computer window full screen for controlling the mouse. When the hands are detected and when we find which finger is up for performing the specific mouse function, a rectangular box is drawn with respect to the computer window in the webcam region where we move throughout the window using the mouse cursor, as for now we hidden that box to get clear view of screen. 
+ we are detecting which finger is up using the tip Id of the respective finger that we found using the MediaPipe and the respective co-ordinates of the fingers that are up, and according to that, the particular mouse function is will be performed using the pyautoGUI python package

![image](https://user-images.githubusercontent.com/79743499/185776089-f127de78-1644-4fd8-887c-c10434430020.png)


+ For performing Gesture control, we will find and set the tip ID for respective operations. 
+ For example: If the index finger is up with tip Id = 1 or both the index finger with tip Id = 1 and the thumb finger with tip Id = 2 are up, the volume of our system can be controlled using the Pycaw package of Python, as shown in Figure 7.2. 
+ Here we just implemented only volume control gesture, like this we can perform more gesture control operation such as slider control, scroll wheel control, tab control etc., using openCV libraries.

![image](https://user-images.githubusercontent.com/79743499/185776128-28a366da-543a-4a6c-b9ef-456a04643308.png)


+ The system combines aspects of the traditional system keyboard with more modern, gesture-based approaches to typing. To enter text, users perform a assigned gesture in which their index finger traces over the letters of their intended word. 
+ For example: If the index finger with tip Id = 1 and the thumb finger with tip Id = 0 are up and the distance between the two fingers is lesser than 30px, the computer is made to perform the button click over the letter, which inputs the letter in system using the pynput Python package, as shown in Figure. 
+ A gesture-based interface in which a user can input data in a hands-free way presents a solution to this requirement.

![image](https://user-images.githubusercontent.com/79743499/185776152-3828128e-61ba-4ba1-90c0-e9b346b0f1fa.png)


+ Our aim is to operate the system without direct interactions. The gesture-control system we implemented will do lot of operations without direct interactions even though, we might need to interact the system to start the gesture control process. 
+ So we included voice assistance, which can help us to start and terminate the process of gesture-control system as shown in Figure. 
+ It works with the pyttsx3 and speech-recognition in python modules which will fetch the word from our voice and convert it to text and recognize it with our command which we assigned with some operations(opening virtual mouse, closing virtual mouse, etc.,).
