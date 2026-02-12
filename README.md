# Attitude-altitude-estimation-system

# Overview

Design and implementation of a low-cost embedded system capable of estimating:

- Orientation (roll and pitch)

- Relative altitude

- Vertical velocity

Using inertial and barometric sensing.

This project simulates fundamental aerospace state estimation principles used in flight control and satellite attitude systems.

# Hardware Platform

- ESP32 (WiFi-enabled microcontroller)

- MPU6050 (6DOF IMU: accelerometer + gyroscope)

- BMP280 (Barometric pressure sensor)

# System Architecture

Sensors → ESP32 → State Estimation → WiFi Telemetry → Python Analysis

# Technical Objectives

- Raw IMU data acquisition via I2C

- Gyroscope bias and drift analysis

- Complementary filter implementation

- Pressure-to-altitude conversion

- Vertical velocity estimation

- Real-time data streaming

- Python-based visualization and logging

# Mathematical Foundation (Planned)

- Rigid body rotation kinematics

- Angular rate integration

- Complementary filtering

- Barometric altitude model

- Basic state estimation principles

# Long-Term Vision

Develop a modular embedded state estimation system that reflects core aerospace engineering concepts in flight dynamics and navigation.
