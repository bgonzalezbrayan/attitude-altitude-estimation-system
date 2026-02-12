# Mathematical Model – Attitude Estimation
# 1. Coordinate Frames

Body-fixed reference frame:

X-axis → Forward

Y-axis → Lateral

Z-axis → Vertical

The gyroscope measures angular velocity:

omega = [omega_x, omega_y, omega_z]

# 2. Roll and Pitch from Accelerometer

Assuming static conditions:

Roll (phi):

phi = atan( a_y / a_z )

Pitch (theta):

theta = atan( -a_x / sqrt(a_y² + a_z²) )

Where:

a_x, a_y, a_z are accelerometer measurements.

Limitations:

Sensitive to vibration

Sensitive to linear acceleration

# 3. Gyroscope Integration

theta(t) = theta(t-1) + omega * delta_t

Problem:

Bias

Drift accumulation over time

# 4. Complementary Filter

theta = alpha * theta_gyro + (1 - alpha) * theta_acc

Where:

0 < alpha < 1

Typical alpha = 0.95 – 0.99

Gyroscope → High-frequency response
Accelerometer → Low-frequency stability

# 5. Barometric Altitude

h = 44330 * (1 - (P / P0)^(1 / 5.255))

Where:

P = measured pressure

P0 = reference pressure at ground level

# 6. Vertical Velocity

v_z = (h(t) - h(t-1)) / delta_t
