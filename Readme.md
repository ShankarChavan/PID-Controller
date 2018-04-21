# PID-Controller(Proportional Integral and Differential)
Driving a vehicle with PID-Control

### Project Basics
------
This project requires to drive a simulated car around a virtual track by controlling the steering angle using PID controller.The Objective was to find the best parameters for PID controller in order to keep car on track. 

### Steps
______
* Implement the PID controller Update and Error function for steering the car.

* Identify the optimized parameter for keeping car on track.


### Challenges & Approach
___
* __Challenge__

Initially after implementing the Update and Total error function, I faced a problem wherein car was always deviating from the lane towards right side as steering angle was not in range of -1 and 1, but after reading udacity discussion blog I was able to resolve the issue.

* __Approach for parameter selection__

I manually selected the parameter for P,I and D after testing them across the track by keeping the throttle constant at 0.3.

Created UpdateThrottle function with max throttle of 0.75 to test car movement with dynamic increase or decrease in throttle.  

Parameters which worked for me were **(P=0.24,I=0.00,D=4.0)** with constant throttle 0.3.

Initially I started with 0.01 for P, and 1.0 for D and 0.001 for I,but  after testing few of them on track I ended up with above parameters.

### Demo videos 
____

All the videos with recording of car running on a track is there in **videos\_demo** folder.

* **P-parameter**: When **P** parameter kept zero car moved steadily but falls out of track while making left turn on track. 

* **I-Parameter**: Keeping **I** parameter to zero didn't impacted the cars movement on track much hence it was chosen in final parameter.

* **D-parameter**: When **D** parameter is kept zero car oscillated in right and left direction and finally falled out of track hence tuning was required for it.


## Basic Build Instructions
____
1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./pid`. 


## Code Style

Please (do your best to) stick to [Google's C++ style guide](https://google.github.io/styleguide/cppguide.html).

## Project Instructions and Rubric

Note: regardless of the changes you make, your project must be buildable using
cmake and make!


## Hints!

* You don't have to follow this directory structure, but if you do, your work
  will span all of the .cpp files here. Keep an eye out for TODOs.





