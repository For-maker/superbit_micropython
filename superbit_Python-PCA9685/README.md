# Superbit Microbit Python Driver for PCA9685

A simple python class for using the Superbit for PCA9685.

#### Using the driver

There is an example of how to use the driver to control a server in main.py but it can be used to control motors and LEDS as well. The example sets the servo at channel 0 to it's minimum value, sleeps for 1 second, then set's channel 0 to it's maximum value:
```
pwm.set_pwm(0, 0, servo_min)
sleep(1000)
pwm.set_pwm(0, 0, servo_max)
sleep(1000)
```
If you do not know how to load additional files onto your microbit (so main.py can read the PCA9685 driver from PCA9685.py) read https://microbit-playground.co.uk/howto/add-python-module-microbit-micropython.

#### Servo helper

There is now a servo helper class in servo.py based on https://github.com/adafruit/micropython-adafruit-pca9685/blob/master/servo.py that makes it easier to set a servo position in degrees (the default), radians, microseconds or directly as a number between 0 and 4095 signifying the duty cycle. There is an example using degrees in the main.py that also demonstrates the 'release' method that stops sending a message to the servo, releasing it.

#### Acknowledgement

This driver is adapted from Tony DiCola's driver at https://github.com/adafruit/Adafruit_Python_PCA9685/blob/master/Adafruit_PCA9685/PCA9685.py
