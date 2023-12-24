# Face-KeyPoint-Detection
To Detect key points on face Image and it covers 15 points 

## Data Used is from kaggle FaceKey point Detection 
also practiced how to use own custom data 
### **What is Haar Casacade Method??**
The Haar cascade classifier is based on Haar features, which are
the sum of the difference of pixel values in a rectangular region. The magnitude of the
difference value is calibrated to indicate the characteristics of a given region in the face—for
example, nose, eyes, and so on.

---
![image1](https://github.com/prateekghorawat/Face-KeyPoint-Detection/blob/main/images/image1.jpeg)
* The rectangle section is placed over the characteristic feature of the face. 
* As the intensity of the eye region is darker than the face, the black region of the rectangle goes near
the eye and the white region goes below the eye. 
* Similarly, as the nose region is brighter
than its surroundings, the white rectangle goes on the nose and the black rectangles rest on 
the two sides.
* The value of the Haar like feature can be calculated as the difference between
sum of the pixel values in the white region and the sum of the pixel values in the
black region.

---

![image2](https://github.com/prateekghorawat/Face-KeyPoint-Detection/blob/main/images/image2.png) 
![image3](https://github.com/prateekghorawat/Face-KeyPoint-Detection/blob/main/images/image3.png) 
![image4](https://github.com/prateekghorawat/Face-KeyPoint-Detection/blob/main/images/image4.png) 

**The overall training system was developed to maximize the detection rate and minimize
the false-positive rate.**

* The number of features in each layer of the cascade detector is increased until the
target detection rate and the false-positive targets are achieved for that layer.
* Another stage is added if the overall false-positive rate is not low enough.
* A rectangular feature is added to the current stage until its target rates have been
met.
* The false-positive target from the current stage is used as a negative training set
for the next stage.

---

**The Viola-Jones method is not well suited to handle these
varieties of different facial expressions, and so we need to use the Viola-Jones method for
face detection and then apply the neural network to determine facial key points within the
face's bounding box.**

----

**We can use kaggle dataset directly that contain key points. 
but in order to learn I am creating few of data on my own and than will use kaggle dataset**

https://www.kaggle.com/c/facial-keypoints-detection

--- 

### **Steps for Key Point Detection**

1. Specify the path of Haarscade Classifier. 
2. Define Video Cam.
3. The camera frame reads data using cam.read() and then within each frame, the face is detected using the Haar cascade detector.

**Note :  A bounding
box is drawn around the detected face with (x,y,w,h) parameters. Using the
cv2.imshow parameter, only the detected face is shown on the screen**

4. Resize Image
5. Save the Images 
6. Use Annotator to Annotate 
7. Use Pre-processing on producced CSV.

