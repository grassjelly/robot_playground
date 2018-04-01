# robot_playground
 [Jackal](https://www.clearpathrobotics.com/jackal-small-unmanned-ground-vehicle/) Simulation running on Linorobot's Navigation Stack parameters.

This package creates a shim to Jackal's Gazebo simulator so you can run a virtual robot on Gazebo and try Linorobot's Navigation Stack parameters.

A forked [verion](https://github.com/grassjelly/jackal) of Jackal is used so that the frames and topics on the virtual robot match Linorobot's. You can check out the following commits to see what changes have been made to make Jackal and Linorobot compatible.

- [remapping of Laser's 'front/scan' topic to 'scan' topic](https://github.com/grassjelly/jackal/commit/edf8c5cf8bd3ab2648ed4a37824995f624ee5ce2)
- [remapping of Laser's 'front_laser' frame to 'laser frame'](https://github.com/grassjelly/jackal/commit/505f6c324f3fcbdd11de7414aac37039dc8d8aa9)
- [remapping of Base's 'base_link' frame to 'base_footprint frame'](https://github.com/grassjelly/jackal/commit/6aaabba108f841097a35dd87aecfaf8b6b8d8be9)
- [defining 'base_footprint' frame as base_frame_id on jackal_velocity_controller](https://github.com/grassjelly/jackal/commit/423cfaa99db4b0cec3e8b72f30d3b9c5a38d8bd9)

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