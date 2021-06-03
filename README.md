# Master Thesis: Operator 4.0

Repos Guide:
- Operator4.0_HoloLens2 -> Unity application of the Supervision and Monitoring System
- Operator4.0_ROS -> ROS package of the Programming be Demonstration System
- ExtractCoordinatesHTCvive -> Unity Application for HTC Vive of the initial Accuracy and Repeatability Tests
- repeatability_tests -> ROS package of the initial Accuracy and Repeatability Tests

## Programming Robots by Demonstration using Augmented Reality

The world is living the fourth industrial revolution, Industry 4.0; marked by the increasing intelligence and automation of manufacturing systems. Nevertheless, there are types of tasks that are too complex or too expensive to be fully automated, it would be more efficient if the machine were able to work with the human, not only by sharing the same workspace but also as useful collaborators. A possible solution to that problem is on human-robot interactions systems, understanding the applications where they can be helpful to implement and what are the challenges they face.

In this context a better interaction between the machines and the operators can lead to multiples benefits, like less, better, and easier training, a safer environment for the operator and the capacity to solve problems quicker. The focus of this dissertation is relevant as it is necessary to learn and implement the technologies which most contribute to find solutions for a simpler and more efficient work in industry. This dissertation proposes the development of an industrial prototype of a human machine interaction system through Extended Reality (XR), in which the objective is to enable an industrial operator without any programming experience to program a collaborative robot using the Microsoft HoloLens 2.

The system itself is divided into two different parts: the tracking system, which records the operator’s hand movement, and the translator of the programming by demonstration system, which builds the program to be sent to the robot to execute the task. The monitoring and supervision system is executed by the Microsoft HoloLens 2, using the Unity platform and Visual Studio to program it. The programming by demonstration system’s core was developed in Robot Operating System (ROS). The robots included in this interface are Universal Robots UR5 (collaborative robot) and ABB IRB 2600 (industrial robot). Moreover, the interface was built to easily add other robots.


![overview](https://user-images.githubusercontent.com/76999213/120650117-5c148b00-c475-11eb-8217-522a48f8dac7.png)

## Instructions on how to use

1. The Unity application which is on the *Operator4.0_HoloLens2* folder needs to be installed in the HoloLens2. The installation can be done through the Unity interface, and the version used for the application was 2019.4.2f1.
2. Therefore, you should open the Unity application through Unity Hub.
3. After opening the application in Unity, be careful to change the IP address (go to RosConnector object -> Inspector -> *Ros Bridge Server_IP*) to the IP of the computer where ROS will be running.
4. Then, you should install the application into the headset. To do that open the Build Window and go to Deploy Options. After connecting the HoloLens 2 to the computer, you should click on Test Connection to verify that it is indeed connected.
5. After that, just click on *Build all, then Install*. It may take a few minutes depending on the computer, but when finished, the application is ready to be launched in the headset.
6. Now, switching to the ROS environment, the ROS package included in the folder *Operator4.0_ROS* should be copied to the catkin workspace and then built. To do that through the terminal, type the following commands.
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/inesosoares6/Operator4.0_ROS.git
$ cd ~/catkin_ws
$ catkin_make
```

7. On a terminal type the following instruction to install the [rosbridge_server](https://github.com/RobotWebTools/rosbridge_suite):
```
$ sudo apt install ros-melodic-rosbridge-server
```

9. By this point, all the necessary software is installed and ready to run.
10. The HoloLens 2 application itself gives the necessary instructions on how to use it, however in [this page](https://github.com/inesosoares6/Operator4.0_HoloLens2) is done an overview on how it works.
11. For further details on how the ROS package works, [this page](https://github.com/inesosoares6/Operator4.0_ROS) clarifies what scripts to execute and what they do.

Note: To execute the project as a whole, you should first execute the commands in ROS and then launch the application in HoloLens 2. This is extremely important, because as soon as the application is lauched, it will try to connect to ROS bridge, so that should be already running.

## Author
Inês de Oliveira Soares (ines.o.soares@inesctec.pt | up201606615@up.pt)
- Master Student - Electrical and Computer Engineering @ FEUP
- Master Thesis Development @ INESC TEC
