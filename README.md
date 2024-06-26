# URScript Tutorials
Tutorials for programming UR robots using URScript files.

## Simulating UR robots
If you do not have a UR robot, you can use its simulation by downloading a virtual machine containing the simulation of the robot and the controller.
For an e-Series robot, you can download the version 5.12.6 LTS of Polyscope from the following link:
- [OFFLINE SIMULATOR - E-SERIES - UR SIM FOR NON LINUX 5.12.6 LTS](https://www.universal-robots.com/download/software-e-series/simulator-non-linux/offline-simulator-e-series-ur-sim-for-non-linux-5126-lts/)

## Programming Manual Reference
The URScript programming manual is available from the following link
- [SCRIPT MANUAL - E-SERIES - SW 5.12](https://www.universal-robots.com/download/manuals-e-seriesur20ur30/script/script-manual-e-series-sw-512/)

## Guidelines
URScript is a python-based scripting launguage.

### Reference Frame
The base frame in Polyscope is located according to the following picture
<div align="center">
    <img src="images/readme/00.png", width="700">
</div>

### Adding a URScript to the Robot program
1. From Main Panel select: `Program -> Advanced -> Script`
2. Add the script to the `Robot Program` and select the file containing the instructions
<div align="center">
    <img src="images/readme/01.png", width="700">
</div>
3. For convenience, add a script containing all global variables within a Before Start sequence
<div align="center">
    <img src="images/readme/02.png", width="700">
</div>

### Pose Vectors and Rotations in URScript
A pose is declared using `p` before the `[]` (otherwise it is considered as a list). Example:
```
pose = p[pos_x, pos_y, pos_z, rotVec_x, rotVec_y, rotVec_z]
```
Note that the rotation is described using the Rotation Vector notation. If you want to set a desired Roll-Pitch-Yaw angle, please use the converting function:
```
r = p[pos_x, pos_y, pos_z, rotVec_x, rotVec_y, rotVec_z]
```