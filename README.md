# omni-system

Instructions to get pose data from omnimagnet system eddy current experiments

1. Kill all processes in all terminals (ctrl + c in all terminals), then close all terminals
2. Open a new terminal (ctrl + alt + t) and run `roscore`
3. Open a new terminal and run `rviz`
4. Go to File>Open Config then select the config file at `/home/travis/catkin_ws/src/omniSystem/rviz`
5. Open a new terminal and run `cd catkin_ws`
6. Run `rosrun listener listener.py`
7. Open the file explorer and locate the `.bag` file you wish to extract the pose data from. Single click on the file and press ctrl + c
8. Open a new terminal and run `rosbag play FILENAME -r 10` with ctrl + shift + v in place of `FILENAME`. The number after `-r` is the playback speed.
9. When the experiment finishes playing back, run ctrl + c in the terminal that is running `listener.py`

The data is saved as `test.csv` in `~/catkin_ws/`. Rename it (F2) and relocate it.

The data is saved in the following format: x, y, z
