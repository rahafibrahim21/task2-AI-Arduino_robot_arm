# task2-AI-Arduino_robot_arm
1-install arduino_robot_arm package to "src" folder
2- open terminal
3- writing commands
cd ~/catkin_ws/src sudo apt install git git clone https://github.com/smart-methods/arduino_robot_arm.git

install all the dependencies
cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-noetic-moveit

sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

close terminal

*Configuring Arduino with ROS
1-Install Arduino IDE in Ubuntu https://www.arduino.cc/en/software to install run write in terminal

$ sudo ./install.sh after unzipping the folder

2-Launch the Arduino IDE

3-Install the arduino package and ros library http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup

4-Make sure to change the port permission before uploading the Arduino code $ sudo chmod 777 /dev/ttyUSB0

*install rosserial for Arduino by :
write in termina

sudo apt-get install ros-indigo-rosserial-arduino

sudo apt-get install ros-indigo-rosserial

*creates the ros_lib directory.
d/libraries

rm -rf ros_lib

rosrun rosserial_arduino make_libraries.py .

##Runing
*Controlling the robot arm by joint_state_publisher in the terminal
$ roslaunch robot_arm_pkg check_motors.launch
*Controlling the robot arm by Moveit and kinematics
$ roslaunch moveit_pkg demo.launch




