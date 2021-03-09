# rviz_ws

My Overlay Workspace for RViz

## Prerequisites

- ROS2 Foxy

## Usage

```sh
# Clone repositories
git clone git@github.com:kenji-miyake/rviz_ws.git
cd rviz_ws
mkdir src
vcs import src < workspace.repos

# Build workspace
colcon build --cmake-args -DCMAKE_BUILD_TYPE=Release

# For workspace overlay
echo "source ~/rviz_ws/install/setup.bash" >> ~/.bashrc
source ~/.bashrc

# Build your workspace
cd YOUR_COLCON_WORKSPACE
colcon build --symlink-install --cmake-args -DCMAKE_BUILD_TYPE=Release
```
