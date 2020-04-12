# OTTO
The automated micropipette

OTTO is an open-source liquid handler that can automatically prepare samples for qPCR, flow cytometry, and other biological assays that rely on accurate liquid dispensing. It features designs that optimize speed and accuracy, unattended automation, and modular components, all with easily sourceable or 3D-printed parts. In total, OTTO only costs approximately $1000 and works with most commercially available micropipettes and plastic labware, so you can use materials you already own.

<iframe width="560" height="315" src="https://www.youtube.com/embed/qub5chyIQ0s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

We created an interactive 3D model of OTTO, hosted by Onshape, to make it easy to see how all of the mechanical components fit together physically: 

<iframe src="https://myhub.autodesk360.com/ue2df3503/shares/public/SH56a43QTfd62c1cd96832754d64d89c2831?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


OTTO uses custom firmware to feed G-code into an Arduino Due, which controls the step and direction of stepper motors that drive the machine. All of these components work in tandem to form a robust, accurate, and reliable automated liquid handling system for generating reproducible data at an affordable price point.

The necessary components of our design, including materials and set-up instructions, are all separated and detailed in the <a href="mechanical.md">Mechanical</a>, <a href="electrical.md">Electrical</a>, and <a href="software.md">Software</a> descriptions. All files are linked in each section, and can also be found in the GitHub repository: https://drd-flo.github.io/OTTO/.

### License
OTTO is distributed under the [MIT License](https://github.com/pachterlab/poseidon/blob/release/LICENSE)

------------
# Mechanical Systems

<iframe width="560" height="315" src="https://www.youtube.com/embed/qub5chyIQ0s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe src="https://myhub.autodesk360.com/ue2df3503/shares/public/SH56a43QTfd62c1cd96832754d64d89c2831?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Work Envelope
OpenBuilds’ open-source linear rails were used as both the linear motion rails and the frame for the system. Specifically, V-rails were chosen because of their ability to easily connect to form the work envelope. The work envelope contains all of the accessories required for an experiment (e.g., tip boxes, well plates, etc.), as well as the pipette tip sensors, attached to the bottom with 3D-printed holders and fasteners.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201C.png)
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201D.png)

## Axes
The linear actuator of the X-axis is a timing belt/pulley configuration to maximize speed. 8-mm lead screws were used for the Y- and Z-axes for increased stability and accuracy.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201A.png)

## Gantry
Our design utilizes a gantry system to take advantage of higher accuracy and more work space if needed. The Z- and X- axes form the gantry assembly, which rides on a pair of linear rails and lead screws that comprise the Y-axis.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201B.png)

## Pipetting Assembly
A Haydon Kerk® captive linear stepper motor comprises the pipetting linear actuator. It sits above the micropipette and automates the pressing of the plunger on the micropipette.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201A.png)

## Floating Head Assembly
The pipetting assembly rides on a pair of vertical, spring-loaded linear rods to create the floating head assembly. The spring constants of the springs used determine the micropipette’s tip loading pressure. The entire assembly includes a plate attached to V-wheels, which ride on the linear rails of the gantry.
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/Figure%201B.png)

---------
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
![](https://raw.githubusercontent.com/hannahchenx/hannahchenx.github.io/master/wiring%20diagram.jpg)

# Software 

## Script
The Python script was created using a Python 3 application that features a Tkinter graphical user interface (GUI). The script is available here. 
[Image of an example of the user interface]

## Arduino
Upload the custom firmware, available here, to the Arduino Due. Connect it to a USB port on a computer, then place the jumpers on the appropriate locations on the Arduino and connect them to the motors on the other end.
[image or flow chart of how everything should be connected]

## Running the program
[Instructions?]



