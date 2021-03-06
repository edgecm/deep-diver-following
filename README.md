This is a container for an autonomous diver-following project. Deep object detection models are used for diver (and other objects such as ROV) detection. A simplified version of that is utilized for autonomous tracking (and following) of a single diver by an underwater robot. The ROS version, tested on Aqua-8 robot, is provided in the diver_following_cnn folder.

- Paper:  https://ieeexplore.ieee.org/document/8543168
- Dataset information:  https://onlinelibrary.wiley.com/doi/full/10.1002/rob.21837 
- Frozen graph of a trained (SSD MobileNet) model: provided in model_data folder
- Weights for the CNN-based model proposed in the paper: available on request
- Important packages: Python 2.7, OpenCV 3, TensorFlow 1.11.0 (with object detection API)

## Testing the detector
Use the [test_detector.py](test_detector.py) file for testing detection performances on individual images.

| Single diver | Multiple divers | Divers and ROVs | 
|:--------------------|:--------------------|:----------------|
| ![det-7](/test_data/res/6.jpg) | ![det-7](/test_data/res/7.jpg)     | ![det-1](/test_data/res/1.jpg) |


## Testing the diver-tracker 
For testing diver-tracking on a video or sequences of images, use the [test_diver_tracker.py](test_diver_tracker.py) file. A couple of videos and image sequences are provided in the test_data folder. Change the argument values to test other files.


#### Demo: https://youtu.be/9xukzT8dqzQ

| frame t | frame t+n | frame t+2n | 
|:--------------------|:----------------|:----------------
| ![det-86](/test_data/res/86.jpg)     | ![det-96](/test_data/res/96.jpg) |   ![det-106](/test_data/res/106.jpg) | 
| ![det-1118](/test_data/res/1118.jpg)     | ![det-1138](/test_data/res/1138.jpg) |   ![det-1158](/test_data/res/1158.jpg) | 




## ROS version
- The diver_following_cnn folder contain the ROS-kinetic package version 
- This version is currently running on the Aqua MinneBot robot (more details: http://irvlab.cs.umn.edu)
- Feel free to cite the paper you find anything useful:  https://ieeexplore.ieee.org/document/8543168
```
@article{islam2018towards,
  title={{Toward a Generic Diver-Following Algorithm: Balancing Robustness and Efficiency in Deep Visual Detection}},
  author={Islam, Md Jahidul and Fulton, Michael and Sattar, Junaed},
  journal={{IEEE Robotics and Automation Letters (RA-L)}},
  volume = {4},
  number = {1},
  pages = {113--120},
  year={2018},
  publisher={IEEE}
}
```
