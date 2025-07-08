
---

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ManchesterRoboticsLtd/Puzzlebot/blob/main/Misc/Logos/Puzzle_Bot_Logo_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/ManchesterRoboticsLtd/Puzzlebot/blob/main/Misc/Logos/Puzzle_Bot_Logo_B.png">
  <img alt="Shows MCR2 logo in black or white." width="250" align="right">
</picture>


 <div id="user-content-toc">
  <ul align="center" style="list-style: none;">
    <summary>
      <h1>Puzzlebot Gazebo Simulator</h1>
    </summary>
  </ul>
</div>

---


# Introduction

The **Puzzlebot Gazebo Simulator** is a full 3D Gazebo, ROS 2-based simulation environment for testing and developing robotics algorithms on virtual Puzzlebot models. It provides realistic physics, sensor emulation, and world environments for autonomous navigation, perception, and control experiments.

---

## 🚀 Features

- 🔧 Simulates multiple Puzzlebot variants (Hacker, Jetson, Jetson + LiDAR)  
- 🌍 Rich Gazebo environments including arenas and obstacle courses  
- 📷 Sensor simulation: Camera, Time-of-Flight (ToF), LiDAR
- 🧠 ROS 2 compatible (Humble/Foxy)  
- 🕹️ Compatible with Gazebo Garden  

---

## 👥 Who Is This For?

🏫 Robotics educators and students (university-level)

🧪 Researchers in SLAM, control, or perception

⚙️ Developers preparing ROS 2 algorithms before real robot deployment

---

## 🧰 Repository Contents

- `puzzlebot_description/` – URDF and models for all Puzzlebot variants  
- `puzzlebot_gazebo/` – Gazebo worlds, launch files, and plugins  
- `launch/bringup_simulation_launch.py` – Main launch file with full configuration  
- `worlds/` – Custom environments (.world/.sdf)

---

## 📦 Installation

1. **Clone the repository into your ROS 2 workspace:**

```bash
cd ~/ros2_ws/src
git clone https://github.com/your-org/puzzlebot-gazebo-simulator.git
cd ~/ros2_ws
colcon build
source install/setup.bash
```

2. (Optional): If using WSL or experiencing rendering issues:
```
export LIBGL_ALWAYS_SOFTWARE=1
```

3. **Follow the configuration instructions in the Manual *MCR2_Puzzlebot_Gazebo_Sim_Simulator***

---

## Installing Gazebo Garden
```
sudo apt-get update
sudo apt-get install lsb-release curl gnupg
sudo curl https://packages.osrfoundation.org/gazebo.gpg --output /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null
sudo apt-get update
sudo apt-get install gz-garden
```

### Running Gazebo Garden
```
gz sim
```
### Installing ROS Bridge for Humble
```
sudo apt-get install ros-humble-ros-gzgarden
```
Alternatively, you can follow the instructions [here](https://github.com/gazebosim/ros_gz) either from binary or source. Check the table for compatibility. 
