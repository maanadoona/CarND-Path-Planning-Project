# CarND-Path-Planning-Project
Self-Driving Car Engineer Nanodegree Program

[image0]: ./result/lane0_blocked.png
[image1]: ./result/lane0_toright.png
[image2]: ./result/lane1_blocked.png
[image3]: ./result/lane1_toLeft.png
[image4]: ./result/lane1_toright.png
[image5]: ./result/lane2_blocked.png
[image6]: ./result/lane2_toleft.png
[image7]: ./result/strategy.png


## Project Goal
In this project your goal is to safely navigate around a virtual highway with other traffic that is driving +-10 MPH of the 50 MPH speed limit. You will be provided the car's localization and sensor fusion data, there is also a sparse map list of waypoints around the highway. The car should try to go as close as possible to the 50 MPH speed limit, which means passing slower traffic when possible, note that other cars will try to change lanes too. The car should avoid hitting other cars at all cost as well as driving inside of the marked road lanes at all times, unless going from one lane to another. The car should be able to make one complete loop around the 6946m highway. Since the car is trying to go 50 MPH, it should take a little over 5 minutes to complete 1 loop. Also the car should not experience total acceleration over 10 m/s^2 and jerk that is greater than 10 m/s^3.

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./path_planning`.


## Implementation
 I made a strategy to avoid a collision and for safe driving.
 The below drawing shows detection area. First I check the where is the car, exactly which side of ahead, left and right.
 Then I decide where to go? It depends on which lane I'm in and which side is blocked from other car.

![alt text][image7]


## Simulation Result

### case 1. Driving through lane 0 and obstacle ahead and right
==> Keep the current lane
![alt text][image0]

### case 2. Driving through lane 0 and obstacle ahead
==> to right
![alt text][image1]

### case 3. Driving through lane 1 and obstacle ahead, left and right
==> Keep the current lane
![alt text][image2]

### case 4. Driving through lane 1 and obstacle ahead and right
==> to left
![alt text][image3]

### case 5. Driving through lane 1 and obstacle ahead and left
==> to right
![alt text][image4]

### case 6. Driving through lane 2 and obstacle ahead and left
==> Keep the current lane
![alt text][image5]

### case 2. Driving through lane 2 and obstacle ahead
==> to left
![alt text][image6]


### Rules check
#### 1. At lease 4.32 miles without incident
 ==> From above images, you can check the result. I have driven safely almost 30minutes and 20miles over.
 
### Speed limit
 ==> I set the MAXIMUM Speed is 49.5 miles/h
 
### Acceleration and Jerk
 ==> Acceleration and jerk are also not exceed.
 
### collision
 ==> No collisions
 
### Stay in lane
 ==> In 3 seconds, the car change the lane smoothly.
 

 
 
 
 
