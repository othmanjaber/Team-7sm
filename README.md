<div align="center">

![Banner](./other/repository%20images/Team%20logo.png)

[![WRO 2026](https://img.shields.io/badge/WRO-2026%20Future%20Engineers-blue?style=for-the-badge&logo=robot&logoColor=white)](https://wro-association.org/)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)](https://www.instagram.com/axivio2025/)
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://www.youtube.com/@Axivio-e1g)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

**Official documentation for 7sm**

[Watch Demo](#performance-video) • [Documentation](#table-of-contents) • [Build Guide](#robot-construction-guide) 

</div>

---

## Table of Contents
* [The Team](#team)
* [The Challenge](#challenge)
* [The Robot](#robot-image)
* [Mobility Management](#mobility-management)
  * [Powertrain](#powertrain-mechanical)
    * [Drivetrain](#drivetrain-mechanical)
    * [Motor](#motor-mechanical)
    * [Motor Driver](#motor-driver-mechanical)
  * [Steering](#steering-mechanical)
    * [Servo Motor](#servo-motor)
  * [Chassis](#chassis-mechanical)
* [Power and Sense Management](#power-and-sense-management)
  * [Power Supply](#power-supply)
  * [Arduino Mega](#arduino-mega)
  * [bno080](#bno080)
  * [us100](#us100)
  * [Pixy2](#pixy2)
  * [Circuit Diagram](#circuit-diagram)
* [Robot Construction Guide](#robot-construction-guide)
  * [Step 1: Print the 3D parts](#3d-printing)
  * [Step 2: Assemble the steering system](#steering-system-assembly)
  * [Step 3: Attach the wheels](#wheel-attachment)
* [Cost Report](#cost-report)
  * [3D Printing Costs](#3d-printing-costs)
  * [components costs](#components-costs)
* [License](#License)

---

## The Team <a class="anchor" id="team"></a>

<div align="center">

</div>

<tr>
<td align="center" width="50%">
</td>

<td align="center" width="50%">
<h3>Othman Jaber</h3>
<img src="other\othman.gif" width="390" align="right" alt="Othman Jaber">
<p> <b>Age:</b> 16</p> <p><b>Email:</b> othmanjaber78@gmail.com</p><p><b>School:</b>King Talal Secondary School</p><p><b>GitHub:</b> <a href="https://github.com/othmanjaber">othmanjaber</a></p><br clear="right"/> <hr> <h3>
</td>

---

<td align="center" width="50%">
<h3>Rayan Rinno</h3>
<img src="other\rayan.gif" width="390" align="right" alt="Rayan Rinno">
<p> <b>Age:</b> 14</p> <p><b>Email:</b> rinoorayan14@gmail.com</p><p><b>School:</b> British Scientific School</p><p><b>GitHub:</b> <a href="https://github.com/rayanrinoo">rayanrinoo</a></p><br clear="right"/> <hr> <h3>
</td>

---

<td align="center" width="50%">

<h3>Yazan Hindia</h3>
<img src="other\yazan.gif" width="390" align="right" alt="Yazan Hindia">
<p> <b>Age:</b> 14</p> <p><b>Email:</b> yazanhindia@gmail.com</p><p><b>School:</b> Mahmoud Darwish School </p><p><b>GitHub:</b> <a href="https://github.com/kdo3l">Yazan Hindia</a></p><br clear="right"/> <hr> <h3>


## The Challenge <a class="anchor" id="challenge"></a>

The **[WRO 2026 Future Engineers - Self-Driving Cars](https://wro-association.org/)** challenge invites teams to design, build, and program a robotic vehicle capable of driving autonomously on a racetrack that changes dynamically for each round. The competition includes two main tasks: completing laps while navigating randomized obstacles and successfully performing a precise parallel parking maneuver. Teams must integrate advanced robotics concepts such as computer vision, sensor fusion, and kinematics, focusing on innovation and reliability.

Learn more about the challenge [here](https://wro-association.org/wp-content/uploads/WRO-2026-Future-Engineers-Self-Driving-Cars-General-Rules.pdf).


## Our Robot <a class="anchor" id="robot-image"></a>

Here are some pictures of our robot from every side:
<table>
<tr>
<td align="center"><img src="./v-photos/front.jpg" width="250"/><br/><b>Front</b></td>
<td align="center"><img src="./v-photos/back.jpg" width="250"/><br/><b>Back</b></td>
<td align="center"><img src="./v-photos/left.jpg" width="250"/><br/><b>Left</b></td>
</tr>
<tr>
<td align="center"><img src="./v-photos/right.jpg" width="250"/><br/><b>Right</b></td>
<td align="center"><img src="./v-photos/top.jpg" width="250"/><br/><b>Top</b></td>
<td align="center"><img src="./v-photos/bottom.jpg" width="250"/><br/><b>Bottom</b></td>
</tr>
</table>
</div>

# Mobility Management <a class="anchor" id="mobility-management"></a>

The robot's mobility is managed by a combination of components, including the powertrain, steering system, and chassis. These elements work together to ensure the robot's smooth and efficient movement.

## Powertrain <a class="anchor" id="powertrain-mechanical"></a>

### Drivetrain <a class="anchor" id="drivetrain-mechanical"></a>

Our drivetrain uses a DC motor that transfers power to the rear axle through an external gear system. This gear arrangement reduces the rotational speed while increasing the available torque, providing smooth and reliable movement. The rear wheels are mounted on a common axle for synchronized rotation, while the front wheels are mounted independently and connected to the steering mechanism. This design offers a good balance between simplicity, durability, and driving performance.

**Potential Improvements**:
- Add a differential system for smoother turning
- Implement encoder feedback for precise distance measurement
- Consider gear reduction for better torque control

### Motor <a class="anchor" id="motor-mechanical"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/ga25-371.jpg" alt="DC Motor" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Voltage: 12V</li>
      <li>Current: 0.4-1 A no load, 3.2A stall</li>
      <li>Speed: ~130 RPM at 12v</li>
      <li>Torque: ~4.4-8 kg.cm</li>
      <li>Weight: 55g</li>
    </td>
  </tr>
</table>

A standard DC gearmotor was selected for its simplicity, reliability, and ability to provide the required torque. The drivetrain uses a simple two-gear transmission, where the first gear is connected to the motor shaft and drives the second gear mounted on the axle. This design efficiently transfers power while maintaining a compact and reliable mechanical structure.

**Potential Improvements**:
- Add encoder for precise speed and position control
- Implement better motor mounting for reduced vibration
- Consider brushless motor for higher efficiency

### Motor Driver <a class="anchor" id="motor-driver-mechanical"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="other/repository%20images/l298n.jpg" alt="L298N Motor Driver" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Power supply voltage: 5V-35V</li>
      <li>Output current: 2A per channel (4A peak)</li>
      <li>Built-in 5V regulator</li>
      <li>Direction and PWM speed control</li>
      <li>Heat sink for thermal protection</li>
    </td>
  </tr>
</table>

We use the L298N motor driver to control both the drive motor and servo motor. This dual H-bridge driver allows precise control of motor direction and speed through PWM signals from the Arduino.

**Potential Improvements**:
- Add current sensing for motor feedback
- Implement better heat dissipation
- Use more efficient motor driver with lower voltage drop


to mount the motor driver we made this 3d design: 

<img src="other/repository images/motor driver holder.png">

## Steering <a class="anchor" id="steering-mechanical"></a>

Our steering system uses an Ackermann steering mechanism for improved turning performance. The front wheels are controlled by a servo motor connected through a mechanical linkage designed to provide different steering angles for the inner and outer wheels during a turn. This reduces tire slipping and allows the robot to follow smoother and more accurate turning paths.

<img src="other\ackermann.gif" width="390" align="right" alt="ackermann steering visualise">

**Potential Improvements**:
- Use stronger servo for more precise control

### Servo Motor <a class="anchor" id="servo-motor"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/mg996r.jpg" alt="Servo Motor" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Weight: 55g</li>
      <li>Stall torque: 9.4 kgf·cm (4.8V ), 11 kgf·cm (6 V)</li>
      <li>Operating speed: 0.17 s/60º (4.8 V), 0.14 s/60º (6 V)</li>
      <li>Rotation angle: 180 degrees</li>
    </td>
  </tr>
</table>

We selected the MG996R servo motor for steering control due to its high torque and durability. The servo provides sufficient power to accurately control the Ackermann steering mechanism, ensuring smooth and precise wheel movement during direction changes.

## Chassis <a class="anchor" id="chassis-mechanical"></a>

Our chassis is built using 3D printed components, designed to be lightweight yet sturdy. The chassis houses all electronic components and provides mounting points for motors, sensors, and other hardware.

The design prioritizes:
- Low center of gravity for stability
- Easy access to components for maintenance
- Proper weight distribution
- Compact form factor

# Power and Sense Management <a class="anchor" id="power-and-sense-management"></a>

The robot's power and sensor management system consists of several components working together to provide reliable power and accurate environmental sensing.

### Power Supply <a class="anchor" id="power-supply"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/li%20ion%20battery.jpg" alt="Power Supply" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Type: Li-Po or NiMH battery pack</li>
      <li>Voltage: 7.4V-9V</li>
      <li>Capacity: 2000-3000mAh</li>
      <li>Discharge rate: 10C-20C</li>
    </td>
  </tr>
</table>

Our power system uses a rechargeable battery pack to provide clean, stable power to all components. The L298N driver includes a built-in 5V regulator to power the Arduino and sensors.

**Potential Improvements**:
- Add battery voltage monitoring
- Implement low battery warning system
- Use higher capacity battery for longer runtime

### Arduino Mega <a class="anchor" id="arduino-mega"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/arduino%20mega.jpg" alt="Arduino Mega" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Microcontroller: ATmega2560</li>
      <li>Flash memory: 256KB</li>
      <li>SRAM: 8KB</li>
      <li>EEPROM: 4KB</li>
      <li>Frequency: 16MHz</li>
      <li>Digital pins: 54</li>
      <li>Analog pins: 16</li>
      <li>Input voltage: 5V</li>
    </td>
  </tr>
</table>

The Arduino Mega serves as the main controller for our robot, managing all sensors and actuators. Its simplicity and extensive library support make it ideal for this application.

**Potential Improvements**:
- Upgrade to faster microcontroller for better performance
- Add external EEPROM for data logging
- Implement wireless communication capabilities

### BNO080 <a class="anchor" id="bno080"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/bno080.jpg" alt="BNO080" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Motion sensing: 3-axis gyroscope + 3-axis accelerometer + 3-axis magnetometer</li>
      <li>Processor: Integrated ARM Cortex-M0+ sensor hub</li>
      <li>Interface: I2C, SPI, UART</li>
      <li>Operating voltage: 1.7V to 3.6V</li>
      <li>Current consumption: ~3.8mA</li>
      <li>Output: Rotation vector, quaternion, Euler angles</li>
    </td>
  </tr>
</table>

The BNO080 is a 9-axis absolute orientation sensor that combines a 3-axis gyroscope, 3-axis accelerometer, and 3-axis magnetometer with an integrated motion processor. It provides accurate orientation data and sensor fusion internally, making it suitable for maintaining straight-line movement and improving turning accuracy.

**Potential Improvements**:
- Calibrate the sensor regularly to reduce drift
- Combine IMU data with wheel encoders for more accurate position tracking

### US100 <a class="anchor" id="us100"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/us100.jpg" alt="US100" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Measurement range: 20mm to 4500mm</li>
      <li>Accuracy: ±10mm</li>
      <li>Interface: UART / Trigger-Echo</li>
      <li>Supply voltage: 3.0V to 5.5V</li>
      <li>Operating frequency: 40kHz</li>
      <li>Current consumption: <20mA</li>
    </td>
  </tr>
</table>

The US100 ultrasonic sensor uses sound waves to measure distance by calculating the time taken for the echo to return. It provides reliable obstacle detection and distance measurement, making it useful for robot navigation and avoiding collisions.

**Potential Improvements**:
- Apply filtering algorithms to reduce measurement noise
- Combine ultrasonic data with IMU and encoder feedback for improved navigation accuracy

### Pixy2 <a class="anchor" id="pixy2"></a>

<table>
  <tr>
    <td width="50%" style="text-align: left;">
      <img src="./other/repository%20images/pixy2.jpg" alt="Pixy2" width="100%">
    </td>
    <td width="50%" style="text-align: left; vertical-align: top;">
      <h3>Specifications:</h3>
      <li>Processor: NXP LPC4330 204 MHz dual core</li>
      <li>Image sensor: Aptina MT9M114</li>
      <li>Resolution: 1296×976</li>
      <li>Frame rate: 60 fps</li>
      <li>Interface: SPI, I2C, UART, USB</li>
      <li>Power consumption: 140 mA typical</li>
    </td>
  </tr>
</table>

The Pixy2 camera provides advanced computer vision capabilities for color detection and object tracking. It can detect colored objects, lines, and even perform simple AI tasks.

**Potential Improvements**:
- Train custom models for specific object detection
- Implement line following algorithms
- Add better mounting for stable image capture

### Circuit Diagram <a class="anchor" id="circuit-diagram"></a>

<img src = "schemes/circuit diagram.png">

