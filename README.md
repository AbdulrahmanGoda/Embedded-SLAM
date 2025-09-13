# Embedded-SLAM
A Lightweight Real-Time SLAM Library in C++ for Resource-Constrained Robots.


Draft
```
/embedded_slam/
│── main.cpp              # Entry point (task scheduling, SLAM loop, goal handling)
│── slam/
│    ├── ekf.cpp          # EKF predict & update functions
│    ├── mapping.cpp      # Occupancy grid / landmark mapping
│    ├── sensor_fusion.cpp# IMU + odometry fusion
│    └── slam.h
│
│── drivers/
│    ├── imu.cpp          # MPU6050 / BNO055 driver
│    ├── lidar.cpp        # RPLidar driver
│    ├── motor.cpp        # Motor control + encoders
│    └── drivers.h
│
│── config/
│    ├── config.h         # Input/output pins, UART/I2C config, robot geometry
│    └── params.h         # Noise covariance (Q, R), map resolution, max speed
│
│── control/
│    ├── pid.cpp          # Low-level PID control
│    ├── planner.cpp      # Path planner (A*, D*, or pure pursuit)
│    └── control.h
│
└── utils/
     ├── math_utils.cpp   # Jacobians, matrix ops (if not using Eigen-lite)
     └── logger.cpp       # Serial / UART debugging
```
