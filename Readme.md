# Project Racer

## Installation

```shell
cd ~/catkin_ws
catkin_make
```

## Usage

### RTABMSLAM Mapping

```shell
roslaunch slam_project world.launch
roslaunch slam_project mapping.launch rtabmap_args:="--delete_db_on_start" rtabmapviz:=false rviz:=true
roslaunch slam_project teleop
rtabmap-databaseViewer ~/.ros/rtabmap.db
```

### RTABMSLAM Localisation

```shell
roslaunch slam_project world.launch
roslaunch slam_project mapping.launch rtabmapviz:=false rviz:=true
```

### Debug time

```shell

source devel/setup.bash

roslaunch slam_project world.launch
roslaunch slam_project teleop.launch
roslaunch slam_project rtabslam.launch rtabmap_args:="--delete_db_on_start" rtabmapviz:=false rviz:=true amcl:=true
roslaunch slam_project rtabviz.launch
rtabmap-databaseViewer ~/.ros/rtabmap.db

```