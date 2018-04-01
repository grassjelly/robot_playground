# robot_playground
 [Jackal](https://www.clearpathrobotics.com/jackal-small-unmanned-ground-vehicle/) Simulation running on Linorobot's Navigation Stack parameters.

## Installation

### Install dependencies

    ./installdep

### Create workspace and clone sources

    mkdir -p playground_ws/src
    cd playground_ws/src
    catkin_init_workspace

    git clone https://github.com/grassjelly/jackal.git
    git clone https://github.com/jackal/jackal_simulator.git
    git clone https://github.com/jackal/jackal_desktop.git
    git clone https://github.com/ros-visualization/interactive_marker_twist_server.git

    cd ../
    catkin_make
    source devel/setup.bash

## Simulation

Running the virtual robot and Gazebo World:

    roslaunch robot_playground bringup_sim.launch

Running gmapping demo:

    roslaunch linorobot slam.launch

Running autonomous navigation:

    roslaunch linorobot navigate.launch


## Navigation Stack Tuning

If you're using this playground to tune your parameters, [here's](http://kaiyuzheng.me/documents/navguide.pdf) a comprehensive tuning guide.