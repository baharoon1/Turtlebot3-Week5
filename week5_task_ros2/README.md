1. Launch Simulation with Map

For TurtleBot3:
export TURTLEBOT3_MODEL=burger
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py

2. Start Navigation2 with Saved Map

(Use the map you generated in Task 3 SLAM):
ros2 launch turtlebot3_navigation2 navigation2.launch.py \
  use_sim_time:=True map:=$HOME/map.yaml

3. RViz2 Workflow

Open RViz2 (will launch automatically with nav2).

Set 2D Pose Estimate → defines initial robot pose.

Set 2D Goal Pose → pick a destination on the map.

Observe:

Global planner (A* or Dijkstra) generates a complete path.

Local planner (DWB) refines movement near obstacles.

5. Validation Checklist

 Map loads correctly in RViz2
 Initial pose set successfully
 Robot moves toward goal autonomously
 Robot avoids obstacles
 Custom robot tested in same scenario
 Short demo video recorded

