# robot_playground
 [Jackal](https://www.clearpathrobotics.com/jackal-small-unmanned-ground-vehicle/) Simulation running on Linorobot's Navigation Stack parameters.

## Installation

Install Jackal's simulation package.

On Indigo:

    sudo apt-get install ros-indigo-jackal-simulator ros-indigo-jackal-desktop

On Kinetic, follow the instructions [here](https://gist.github.com/grassjelly/2aaf4bba739852616f37e1599db12464).

## Simulation

### Running the virtual robot and Gazebo World:
    roslaunch robot_playground bringup_sim.launch

### Running gmapping demo:
    roslaunch robot_playground slam.launch

### Running autonomous navigation:
    roslaunch robot_playground navigate.launch

