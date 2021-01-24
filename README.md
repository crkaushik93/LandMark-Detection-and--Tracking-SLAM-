# LandMark-Detection-and--Tracking-SLAM-

# Project Overview
In this project, you'll implement SLAM (Simultaneous Localization and Mapping) for a 2 dimensional world! You’ll combine what you know about robot sensor measurements 
and movement to create a map of an environment from only sensor and motion data gathered by a robot, over time. SLAM gives you a way to track the location of a robot 
in the world in real-time and identify the locations of landmarks such as buildings, 
trees, rocks, and other world features. This is an active area of research in the fields of robotics and autonomous systems.

# Project Instructions

The project will be broken up into three Python notebooks; the first two are for exploration of provided code, and a review of SLAM architectures,
only Notebook 3 and the robot_class.py file will be graded:

Notebook 1 : Robot Moving and Sensing

Notebook 2 : Omega and Xi, Constraints

Notebook 3 : Landmark Detection and Tracking

You can find these notebooks in the Udacity workspace that appears in the concept titled Project: Landmark Detection & Tracking. 
This workspace provides a Jupyter notebook server directly in your browser.

# objectives

Implement the sense function to complete the robot class found in the robot_class.py file. This implementation should account for a given amount of measurement_noise and 
the measurement_range of the robot. This function should return a list of values that reflect the measured distance (dx, dy) between the robot's position and any landmarks 
it sees.
One item in the returned list has the format: [landmark_index, dx, dy].

Initialize the array omega and vector xi such that any unknown values are 0 the size of these should vary with the given world_size, num_landmarks, and time step, N, parameters.


The values in the constraint matrices should be affected by sensor measurements and these updates should account for uncertainty in sensing.

The values in the constraint matrices should be affected by motion (dx, dy) and these updates should account for uncertainty in motion.

The values in mu will be the x, y positions of the robot over time and the estimated locations of landmarks in the world. mu is calculated with 
the constraint matrices omega^(-1)*xi.

Compare the slam-estimated and true final pose of the robot; answer why these values might be different.

There are two provided test_data cases, test your implementation of slam on them and see if the result matches.


