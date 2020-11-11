Simulation animation deployment with Simulink Compiler and Simulink 3d Animation
- Joint Space Manipulator Trajectory Following Example 

Copyright 2012-2020 The MathWorks, Inc.

This example shows users how to simulate trajectory tracking and visualize it in the deployed standalone executable using Simulink 3D Animation™ and Simulink Compiler. 
This example includes the following files / folder:

myrobot.slx: This file uses the polynomial trajectory block to interpolate five discrete sets of configurations and create continuous trajectories in the configuration space. 
The Joint Space Motion Model simulates the behavior of a robot under motion control and executes the trajectories. 
To visualize the simulation with animiation while the simulation is running, the signal of desired trajectory, actual trajectory and the position are connected to different outports.

myrobotapp_v2.mlapp : this file is the MATLAB App Designer App file, with which we can visualize the manipulator trajectory tracking in the MATLAB App and the deployed App. 
It utilizes the callback function simulink.compiler.setExternalOutputsFcn to process and visulize trajectory tracking data at each simulation step. 

trajectories.mat: this file contains the pre-defined data of three trajectories; 
workcell_kinova.wrl: this is the VRML model for animation of the simulation. 
workcell_textures folder: this includes all the grahics used by the WRML model. 

The use this example, first open the myrobotapp_v2.mlapp file; click the run button in MATLAB to bring up the MATLAB App.  
Start the MATLAB App and you should see the MATLAB figures and the Simulink 3D animation Viewer are updating while the simulation is running.

To compile the simulation as a standalone executable, in MATLAB command window use mcc -e manipulator_deploy.mlapp to generate a standalone executable. For this step Simulink Compiler is required. 
To use this standalone executable, you machine must have MATLAB R2020b or MATLAB Runtime R2020b installed.   

Products needed for using this example (including deployment): 

MATLAB
Robotics System Toolbox
Simulink
MATLAB Compiler
Simulink Compiler
Simulink 3D Animation

