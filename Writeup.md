# Path Planning Project
# [Rubic](https://review.udacity.com/#!/rubrics/1020/view) points

## Compilation
The code compiles correctly. Spline.h file was added to the src folder after the suggestion given in the Q&A video.

## Valid trajectories

### The car is able to drive at least 4.32 miles without incident.
I drove the car for 6-7 miles without any incidents.

### The car drives according to the speed limit.
No message for speed limit violation was displayed.

### Max Acceleration and Jerk are not Exceeded.
No Violation message for jerk and max acceleration were displayed.

### Car does not have collisions.
No collisions.

### The car stays in its lane, except for the time between changing lanes.
The car stays in its lane for most of the time unless it need to switch lane when their is a car going at slow speed in front and its safe to switch to other lane.

### The car is able to change lanes
The Car is able to change lane when their is a slow car in front f it and its safe to switch to other lane.

## Reflection

The solution is divided into 3 main areas :

1. Prediction(line 258 - line 296) : This part of the code deals with the sensor fusion data to make sense of the environment around us. We want answers to questions like :

    -Is there a car in front of us that is very close.

    -Is there a car in left lane that is close which makes lane switch to left unsafe.

    -Is there a car in right lane that is close which makes lane switch to right unsafe.

2. Behavior(line 298 - line 316) : 
This portion of code decides what to do after making sense of the environment from the previous portion (Prediciton). It can be the following decisions :

    -Do we change lanes if we have a car in front of us.

    -Do we slow down our speed if there are no safe lanes to switch.

3. Trajectory Genreation(line 321 - line 410) :
This portion of the code calculates the trajectory of the car to be followed based on the speed and lane output from the behavior portion, car coordinates and past path points.

