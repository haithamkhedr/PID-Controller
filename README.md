# PID-Controller
C++ Implementation of PID controller to control a car in Udacity simulator

### Effect of PID parameters

-The proportional part of the controller tries to reduce the error with an action that is proportioanl to it. It is the main contributor in decreasing the error.
The problem with P-control is overshooting

-The differential part of the controller decreases the overshoot and make the system response faster, but it makes it easily affected by noise.
 It is calculated as derivative of the error with respect to time.
 
-The integral part removes the systematic bias(wheel misalignments) of the system if it exists, by accumulating the error over time and adding it to the overall control action

### Parameter tuning

Tuning of the Kp,Ki,Kd parameters was manually done. I started increasing Kp first until the Car was overshooting then started to increase Kd to reduce that overshoot. The integral term was optional here so I tried Ki = 0.001 and it worked fine. At last the final parameters that worked for me was Kp = .15, Ki = 0.001 ,Kd = 1.0

### Results

The car can drive smoothly on the track as shown in the images below

![ScreenShot](/Screenshots/ss3.jpeg )

![ScreenShot](/Screenshots/ss2.jpeg )

![ScreenShot](/Screenshots/ss1.jpeg )
