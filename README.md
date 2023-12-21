# CERLAB UAV Autonomy Framework
Welcome to the **CERLAB UAV Autonomy Framework**, a versatile and modular framework for autonomous unmanned aerial vehicles (UAVs). This framework comprises distinct components (simulator, perception, mapping, planning, and control) to achieve autonomous navigation, unknown exploration, and target inspection.

**Author**: [Zhefan Xu](https://zhefanxu.com/), Computational Engineering & Robotics Lab (CERLAB) at Carnegie Mellon University (CMU).

![intro](https://github.com/Zhefan-Xu/CERLAB-UAV-Autonomy/assets/55560905/23a78d4f-a7a3-4c68-b80f-c6dbf6b0f090)

## I. Installation Guide
This repo has been tested on ROS Melodic with Ubuntu 18.04 and ROS Noetic with Ubuntu 20.04 and it only depends on the following ROS packages: [octomap](https://wiki.ros.org/octomap), [mavros](https://wiki.ros.org/mavros), and [vision_msgs](https://wiki.ros.org/vision_msgs). Please use the following commands for installation:

```
# step1: install dependencies
sudo apt install ros-${ROS_DISTRO}-octomap* && sudo apt install ros-${ROS_DISTRO}-mavros* && sudo apt install ros-${ROS_DISTRO}-vision-msgs

# step 2: clone this repo to your workspace
cd ~/catkin_ws/src
git clone --recursive https://github.com/Zhefan-Xu/CERLAB-UAV-Autonomy.git

# step 3: follow the standard catkin_make procedure
cd ~/catkin_ws
catkin_make
```
## II. Run Autonomy DEMO
There are several autonomous flight tasks and here we show the most typical ones: **navigation**, **exploration**, and **inspection**. Please note that the default environment and the flight parameters might be different from the demo shown as below. Please check [uav_simulator](https://github.com/Zhefan-Xu/uav_simulator) for how to change a simulation environment and [autonomous_flight](https://github.com/Zhefan-Xu/autonomous_flight) for adjusting flight parameters.

a. Before getting started, please make sure you are in the ```simulation``` branch of the submodule [autonomous_flight](https://github.com/Zhefan-Xu/autonomous_flight) for the following demos (please check [autonomous_flight](https://github.com/Zhefan-Xu/autonomous_flight) for detailed explanations):
```
cd path/to/autonomous_flight
git branch

# if the output says you are not in the simulation branch, please run the following (otherwise please ignore): 
git checkout simulation
cd ~/catkin_ws
catkin_make
```

b. **Autonomous Navigation:**  


https://github.com/Zhefan-Xu/CERLAB-UAV-Autonomy/assets/55560905/31f4e6eb-857c-43d0-a02c-8defa8eea12c


c. **Autonomous Exploration:**


https://github.com/Zhefan-Xu/CERLAB-UAV-Autonomy/assets/55560905/e0d953de-a542-49c3-86ca-b44d77ff7653



d. **Autonomous Inspection:**


https://github.com/Zhefan-Xu/CERLAB-UAV-Autonomy/assets/55560905/0e580d08-7003-4732-a5b0-5d4041f7d3fd


## III. Real Flight & PX4 Simulation

## IV. The Autonomy Modules
This section introduces the funtionality of each autonomy module included in this framework and provides their links for further details.

## V. Citation and Reference:
If you find this work useful, please cite the paper:
```
@inproceedings{xu2023vision,
  title={Vision-aided UAV navigation and dynamic obstacle avoidance using gradient-based B-spline trajectory optimization},
  author={Xu, Zhefan and Xiu, Yumeng and Zhan, Xiaoyang and Chen, Baihan and Shimada, Kenji},
  booktitle={2023 IEEE International Conference on Robotics and Automation (ICRA)},
  pages={1214--1220},
  year={2023},
  organization={IEEE}
}
```
