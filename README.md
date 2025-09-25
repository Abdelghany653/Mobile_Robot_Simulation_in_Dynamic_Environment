# Mobile_Robot_Simulation_in_Dynamic_Environment


## 🔹 Abstract
Mobile robots play an important role in modern applications such as warehouses, service robotics, and autonomous vehicles, where they must operate in **dynamic environments** that include both **static and moving obstacles**. Traditional navigation approaches often rely on expensive sensors like LiDAR or require complex SLAM algorithms for mapping and localization.  

This project presents a **cost-effective alternative**, where a mobile robot is simulated in **ROS and Webots** using only **low-cost sensors**:  
- **Wheel encoders** for odometry (distance and velocity estimation).  
- **Inertial Measurement Unit (IMU)** for orientation and drift correction.  
- **Ultrasonic sensors** for real-time obstacle detection.  

The robot does not construct a global map (no SLAM); instead, it combines **dead-reckoning (encoders + IMU)** with **reactive obstacle avoidance** using ultrasonic sensors. A **path planning algorithm** (e.g., D* or A*) provides a global route to the target, while a **local planner** dynamically adjusts the trajectory to avoid collisions with moving obstacles. Control is achieved through a **PID-based motion controller**, ensuring smooth navigation.  

Simulation results show that the robot can:  
- Successfully follow a planned path toward a target.  
- React in real time to avoid dynamic obstacles.  
- Improve localization accuracy through encoder + IMU fusion compared to encoders alone.  

This work demonstrates that even without LiDAR or SLAM, a mobile robot can navigate effectively in dynamic environments using lightweight sensor fusion and control techniques. It highlights a **low-cost and practical approach** that could be applied to small-scale robots or educational robotics platforms.  


## 🔹 About
This project demonstrates how a mobile robot can navigate in a **dynamic environment** using **ROS** and **Webots**, relying on low-cost sensors:  
- **Encoders** for odometry (distance + velocity estimation).  
- **IMU** for orientation and stability.  
- **Ultrasonic sensors** for detecting nearby obstacles.  

Instead of building a global map (no SLAM), the robot uses **dead-reckoning + obstacle detection** to follow a path and dynamically avoid collisions.


## 🔹 Objectives
- Simulate a mobile robot with IMU, encoders, and ultrasonic sensors.  
- Estimate position and orientation using **odometry + IMU**.  
- Use ultrasonic sensors for **obstacle detection and avoidance**.  
- Apply **path planning** to move towards a target.  
- Navigate safely in an environment with **static and moving obstacles**.  


## 🔹 Methodology / Workflow
1. **Simulation Setup**  
   - Robot modeled in Webots with IMU, encoders, and ultrasonic sensors.  
   - Environment includes walls, static objects, and moving obstacles.
   
## 🔹 Demo
[![Watch the video](demo_thumbnail.png)](dynamic_environment.mp4)

2. **Odometry & IMU Fusion**  
   - Encoders provide wheel rotations → distance traveled.  
   - IMU gives orientation and helps correct drift.  

3. **Obstacle Detection**  
   - Ultrasonic sensors measure distances to obstacles in real time.  

4. **Path Planning & Control**  
   - Global path to the goal (A*).  
   - Local obstacle avoidance using ultrasonic readings.  
   - PID control ensures smooth velocity and direction changes.  


## 🔹 Tools & Technologies
- **ROS 1 (Noetic)**  
- **Webots R2023a**  
- **C++ / Python** (ROS nodes)  
- **RViz** (for visualization)  


## 🔹 Results

