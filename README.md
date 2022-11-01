# **ENPM Project 1 (tuktuk)**

## **File Tree**

```text
kshitij_Project1
+-Assembly
|  +-Assembky.zip
+-Package
|   +-tuktuk
|       +-10 directories
+-Videos
|   +-circle.mp4
|   +-teleop.mp4
+-kshitij_report_project1.pdf
+-README.md
```

## **Installation**

1. Download and extract the files.
2. The folder Package consists of a ROS Package.
3. Copy the package into your workspace and build it using the following command in your terminal

   ```bash
   cd ~/catkin_ws/

   catkin_make
   ```

4. Don't forget to source your files.

   ```bash
   source devel/setup.bash
   ```

   if you are using zsh

   ```bash
   source devel/setup.zsh
   ```

## **Running**

### 1. Teleop

Open a terminal and launch the `template_telop.launch` file.

```bash
roslaunch tuktuk template_teleop.launch
```

This will launch a gazebo world with the robot in it.

To control the robot using teleop open a new terminal and launch the `teleop_template.py` node.

```bash
rosrun tuktuk teleop_template.py
```

The node will display a message on how to control the robot as shown below.

```bash
Control Your Toy!
---------------------------
Moving around:
   u    i    o
   j    k    l
   m    ,    .
q/z : increase/decrease max speeds by 10%
w/x : increase/decrease only linear speed by 10%
e/c : increase/decrease only angular speed by 10%
space key, k : force stop
anything else : stop smoothly
CTRL-C to quit
```

[![Watch the video](https://img.youtube.com/vi/_NiavjUzX28/maxresdefault.jpg)](https://www.youtube.com/watch?v=_NiavjUzX28)
<!-- Video Link: https://youtu.be/_NiavjUzX28 -->

### 2. Circle

Open a terminal and launch the `circle.launch` file.

```bash
roslaunch tuktuk circle.launch
```

This will launch an empty gazebo world and spawn the robot in its center.

Open another terminal and launch the `circle.py` node.

```bash
rosrun tuktuk circle.py
```

This node will publish commands to the robot to move in a circular loop. It also publishes the values to the terminal.

In a new terminal run the `sub.py` node.

```bash
rosrun tuktuk sub.py
```

This node subscribes to the robot commands that are being published and displays them on the terminal.

[![Watch the video](https://img.youtube.com/vi/mnnSfdf46_U/maxresdefault.jpg)](https://www.youtube.com/watch?v=mnnSfdf46_U)

<!-- Video Link: https://youtu.be/mnnSfdf46_U -->

### Credits

This project was made by

- Kshitij Karnawat (kshitij@umd.edu / kshitijkarnawat009@gmail.com)
- Omkar Chittar (ochittar@umd.edu)
