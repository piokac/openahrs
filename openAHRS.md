# openAHRS #

openAHRS is a free open-source Software/Hardware IMU(Inertial Measurement Unit) / AHRS (Attitude Heading Reference System).
Code is released under the GPL v2 license.

# Current functionality #

openAHRS is in beta stage. Software and hardware schematics are available through git or the web interface through github.


---


## Software ##
A 7-state Kalman Filter is implemented, tracking attitude (roll,pitch,yaw) and gyro bias.
There are some demo applications under the test directory which can be run on any platform. The test-kal7 program simulates noisy input data and writes processed information to an octave file.

openAHRS uses the [eigen2](http://eigen.tuxfamily.org/) matrix library.

## AHRS implementations ##

Platform-specific AHRS's are placed inside the AHRSs/ folder. Currently there is an [AVR32 port](http://github.com/cbecker/openahrs/wikis/avr32-ahrs) only.

### Ports ###

  * [AVR32 ATNGW100](http://code.google.com/p/openahrs/wiki/avr32AHRS)


---


# References #

  * [Autopilot](http://autopilot.sf.net)
  * Review of Attitude Representations Used for Aircraft Kinematics, W. F. Phillips and C. E. Hailey
  * An Introduction to the Kalman Filter, Greg Welch and Gary Bishop
  * [Airborne attitude estimation using a Kalman filter](http://fred.unis.no/Kalman/Master_Thesis_Mathieu.pdf)
  * THE SQUARE-ROOT UNSCENTED KALMAN FILTER FOR STATE AND PARAMETER-ESTIMATION, Rudolph van der Merwe and Eric A. Wan
  * A General Method for Approximating Nonlinear Transformations of Probability Distributions, Simon Julier and Jerey K Uhlmann