# Lukas-Kanade-Template-Tracker

- The Lucas Kanade Template tracker has been implemented using python and OpenCV. 
- The repository consists of the code and output videos. 
- The outline of the pipeline followed is shown below. Further information can be found in the reference paper in the repository.


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
![ezgif-4-c60926022cae](https://user-images.githubusercontent.com/48079888/61188817-c38f7a80-a652-11e9-8436-03530e8edbfe.gif)

### Output for Human Tracking
![human gif](https://user-images.githubusercontent.com/48079888/61188839-21bc5d80-a653-11e9-9eec-848c88ab4578.gif)

