# Stanley

### Introduction
The Stanley Controller was developed by **Stanford University** to win the *DARPA 2005 Challenge*. 
It corrects the heading error of a rover while moving to provide the required turing while moving by providing a *closed feedback loop*.

### The Need for Stanley Controller
Traditionally, for a rover to move, it would require to move upto a certain point on a global frame, then stop there and turn again to face to the next point and move up to that point. While this methodology works, it's extremely time consuming and doesn't look very nice. That's where the Stanley Controller comes into picture. 

If we were simply to try turning in the direction of the goal while moving straight, we might overshoot the goal or undershoot it since we might not turn enough as we are constantly moving and the required turning angle is calculated with respect to a fixed position. Therefore, we need to identify the extra heading anglee that needs to be turned to face the next point.

### The Mathematics


### How To Use
__*IF YOU'RE USING ROS MELODIC*__
1. Clone the repository in your desired ROS package. 
2. Go into the folder Stanley and make the file ```StanleySim-Working-Demo.py``` and ```liveplot.py``` executable using the command: 
```
chmod +x StanleySim-Working-Demo.py
chmod +x liveplot.py
``` 
3. Finally, after getting ```roscore``` running and gazebo turned on, run the two files in two different terminal tabs
```
rosrun <your_ROS_package> StanleySim-Working-Demo.py
rosrun <your_ROS_package> liveplot.py
```
4. Voilà. The default path in the code is a _sine curve_. You can change that yourself to whatever you like.
