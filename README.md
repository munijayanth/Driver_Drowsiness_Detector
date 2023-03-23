
# Drivers Drowsiness detector
This is my first Machine learning project which We as a team made in our early 2nd year as a part of Project Exhibition 1.
Yes,we came to know that there are much more sofisticated softwares in the market as well as under research than the one we made but we thought it would be better to start the journey with this approach.
The Target audience are people who can drive 4 or more wheeled vehicles(cars,trucks)
# Motive
This project deals with the situation when the driver is sleepy or not active while driving which is a possibility and happened many times which resulted in many drastic accidents.
our work is mainly focused to prevent such horrible events.
# Methodology
So we did not use convoultion nueral network (that was our thought when we thought of doing this project) but we used the concepts like ,

EAR, as the name suggests, is the ratio of the length of the eyes to the width of the eyes. The length of the eyes is calculated by averaging over two distinct vertical lines across the eyes as illustrated in the figure below.
![image](https://user-images.githubusercontent.com/87426240/167242955-e30057dc-95bd-421e-89c7-ebbf3c76a3e7.png)

Our hypothesis was that when an individual is drowsy, their eyes are likely to get 
smaller and they are likely to blink more. Based on this hypothesis, we expected 
our model to predict the class as drowsy if the eye aspect ratio for an individual 
over successive frames started to decline i.e. their eyes started to be more closed or 
they were blinking faster

Similar to the EAR, the MAR, measures the ratio of the length of the mouth to the 
width of the mouth. Our hypothesis was that as an individual becomes drowsy, 
they are likely to yawn and lose control over their mouth, making their MAR to be 
higher than usual in this state.
![image](https://user-images.githubusercontent.com/87426240/167243114-23f695b0-c575-4733-8271-34838a68e656.png)

The libraries used are:Scipy, imutils, threading,numpy,play sound,argparse,time,dlib,cv2
# Results
The algorithm takes the image frames captured. Then it detects for the face, if it is found then the Region of interest (ROI) is created around the both eyes and 
mouth. From here it calculates the Eye Aspect Ratio (EAR) and lip distance. The Figure was captured while testing our model.
![image](https://user-images.githubusercontent.com/87426240/167243365-d9d3df15-8279-4faa-a634-07c0e5867ca5.png)

If the EAR value calculated by the algorithm is lesser than the threshold value (0.3), then the algorithm sends a Drowsiness Alert is send to the user with an alarm sound.Also, if the lip distance value calculated is greater than the threshold value (20) it sends a Yawn Alert.

<img align="left" width="300" height="300" src="https://user-images.githubusercontent.com/87426240/167243445-c6ce3e59-a50f-480f-880a-3c7446129d10.png">              <img align="center" width="300" height="300" src="https://user-images.githubusercontent.com/87426240/167243456-0a05ea8e-60d7-4a1f-9f5a-2a3b4dc315fa.png">

# Conclusion
Drowsiness detection system developed around the principle of image processing judges the driver’s alertness level on the basis of continuous eye closures With 80% accuracy, it is obvious that there are limitations to the system like Delay in sounding alarm,Orientation of face,Poor detection with spectacles,Problem with multiple faces which we cannot able to overcome but sure those will be not an issue if we enhance this detections by adding Neural networks and  by fine tuning them.

But for now we have successfully designed a prototype drowsiness detection system using OpenCV software which will alert the driver when they are sleepy/tired.
