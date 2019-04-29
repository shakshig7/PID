# PID Control

## Overview
This project implements a PID controller to control a car in Simulator.
The cross track error, speed and angle are send to the controller and steering angle and throttle is received to drive the car.

## Reflection

### Describe the effect each of the P, I, D components had in your implementation.

* The proportional part (P) helps the car to steer in correct direction. It keeps the car towards the central line.
ON using just this part, the car will go out of the road due to overshooting of center line.

* The Integral part(I) is used to control the systematic bias. In the simulator, this part is not much needed as there is no bias. So, a small value can be used. If only this value is used and is high, car will move in circles.

* The Differentiation part (D) is used to reduced the oscillations and overshooting caused by Proportional part(P).It is used as a counteract for the P.

### Describe how the final hyper parameters were chosen.

The final hyper parameters were chosen by trial and error.
The proportional part is used to keep the car in center. A value of 0.2 is used so that it follows the track but it overshoots.
The Integral part was kept low as simulator is not biased. So, a value of 0.004 is used.
The Derivate part is high to control the oscillations and overshooting caused by P. Value used is 3.
