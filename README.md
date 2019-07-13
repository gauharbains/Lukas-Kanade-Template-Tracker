# Lukas-Kanade-Template-Tracker

The Lucas Kanade Template tracker has been implemented using python and OpenCV. The steps and the outline of the steps followed are given below. The repository consists of the code and the output videos. 

## Outline of the Pipeline Followed : 
A brief overview of the steps followed is given below. Technical background and the implementation of the LK tracking algorithm are described in Section 2 of Simon and Matthew's paper. The reference is provided below. 

#### Reference : Lucas-Kanade 20 Years On: A Unifying Framework: Part 1 , Simon Baker and Iain Matthews, CMU-RI-TR-02-16

![pipeline](https://user-images.githubusercontent.com/48079888/61176866-43a3da80-a596-11e9-8c06-0396a159a1f2.JPG)


-  A schematic overview of the Lucas-Kanade algorithm is shown above. The image I is warped with the
   current estimate of the warp in Step 1 and the result subtracted from the template in Step 2 to yield the error
   image. The gradient of I is warped in Step 3, the Jacobian is computed in Step 4, and the two combined
   in Step 5 to give the steepest descent images. In Step 6 the Hessian is computed from the steepest descent
   images. In Step 7 the steepest descent parameter updates are computed by dot producting the error image
   with the steepest descent images. In Step 8 the Hessian is inverted and multiplied by the steepest descent
   parameter updates to get the final parameter updates delta p which are then added to the parameters p in Step 9.
   
 ## Output (Output videos can be found in the repository)
 
### Output for Car Tracking 
![car13](https://user-images.githubusercontent.com/48079888/61176916-24597d00-a597-11e9-8f1d-6944d5e8d4f5.jpg)
![car168](https://user-images.githubusercontent.com/48079888/61176918-29b6c780-a597-11e9-8e87-15cd7c5c06a5.jpg)
### Output for Human Tracking
![human2](https://user-images.githubusercontent.com/48079888/61176920-33d8c600-a597-11e9-92d2-f5c2f1b78c82.jpg)
![human182](https://user-images.githubusercontent.com/48079888/61176923-3a673d80-a597-11e9-823b-138a055cf868.jpg)
