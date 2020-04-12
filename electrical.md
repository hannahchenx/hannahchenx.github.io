# Electrical Systems 

## Stepper Motor system
A 32-bit Arduino Due receives high-level input from a computer via USB serial connection, which then outputs signals to a trinamic TMC-2660 stepper driver. The stepper driver then rotates bipolar hybrid stepper motors that move the timing belt (X-axis) and lead screws (Y- and Z-axes) at 3200 steps per rotation through microstepping.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%202.png)

## Limit Switches
Mechanical limit switches are at the maxima of each axis to establish a repeatable coordinate system and allow for a common home position to be found.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201C.png)

## Pipette Tip Sensors
Two Balluff through-beam sensors are attached to the bottom of the work envelope to check the concentricity of the micropipette’s tip holder compared to its barrell and to detect the presence of pipette tips.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201C.png)

## Power Supply
A 350W 24V regulated DC power supply powers the motors, limit switches, and through-beam sensors. The 24V output signals of the limit switches and through-beam sensors are converted to the Arduino Due’s 3.3V logic level through optocouplers. 
[A wiring diagram for all the electrical systems with part numbers OR a link to that]

