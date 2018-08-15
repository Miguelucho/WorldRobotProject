
# World Robot Project
__Implementation of SLAM from a model robot in a simulated environment__

The project presented in this repository focuses on implementing simultaneous localization and mapping (SLAM)
using two sensors (Lidar RGB-D sensor and Kinect camera) installed in a two-wheeled robot. The environments that will be mapped are two different worlds that are simulated in Gazebo. The robot transits each environment separately and maps the environment using the GraphSLAM approach to mapping based on appearance in real time (RTAB-Map).

---
#### Launch and load the project.

Do you remember how to use ROS?
It does not matter, here goes a help.

- Open a terminal window:

``Ctrl + Alt + T``

- We started by cloning the project repository:
```bash
$ git clone git://github.com/Miguelucho/WorldRobotProject.git
$ cd WorldRobotProject/catkin_ws/src
$ catkin_init_workspace``
$ cd ..
$ catkin_make
 ...  [ Wait ] ...
$ source devel/setup.bash
```
You now have two new directories: build and devel. The aptly named build directory is the build space for C++ packages and, for the most part. The devel directory does contain something of interest, a file named setup.bash. This setup.bash script must be sourced before using the catkin workspace.

With all the previous steps completed, the project is loaded.

To launch the project there are two options:

##### Option 1.

- Open four (4) terminals: `` Crl + Alt + T`` [As shown in the image]
- In each terminal window:
  - Go to the directory: `` $ cd WorldRobotProject/catkin_ws``
  - Build the workspace: `` $ catkin_make``
  - Load the source: `` $ source devel/setup.bash``
  - Load one node per terminal. [As it appears in the image]

    - `` $ roslaunch udacity_map world.launch``
    - `` $ roslaunch udacity_map teleop.launch``
    - `` $ roslaunch udacity_map mapping.launch``
    - `` $ roslaunch udacity_map rviz.launch``

![Screenshot](/catkin_ws/img/readme.png)

##### Option 2.

- Open one (1) terminal.
- Go to the directory of project: `` $ cd WorldRobotProject``
- Give permissions to the file *rtab_run.sh*: `` $ chmod +x rtab_run.sh``
- Launch the scrip rtab_run: `` $ ./rtab_run``

## Important.
__In the project folder, there is a file '' Write Up '' [English / Spanish] that contains a more detailed description of the project and the author recommends reviewing.__
