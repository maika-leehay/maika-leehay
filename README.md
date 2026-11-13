# Abdelmounaim Mekaoui

**Embedded Systems, Autonomous Robotics (ROS 2) & Cyber-Physical Security Engineer**  
*B.Eng. Computer Engineering (Senior) @ Chengdu Technological University (CDTU)*

[https://img.shields.io/badge/C%2B%2B-17-00599C?logo=cplusplus]
[https://img.shields.io/badge/ROS_2-Jazzy_Jalisco-22314E?logo=ros]
[https://img.shields.io/badge/Embedded-STM32_%7C_ESP32_%7C_FreeRTOS-03234B]
[https://img.shields.io/badge/Compliance-ISO_21434_%7C_ISO_10218:2025_%7C_EU_CRA-success]

I engineer deterministic **C++17 microcontroller firmware**, **ROS 2 autonomous navigation & perception pipelines**, and **cyber-physical security architectures**—bridging physical sensors and actuators (`STM32`, `ESP32`, `SocketCAN`) with edge AI and industrial safety standards.

## Flagship Engineering Repositories

### 1. [Cyber-Physical Robotics, Edge AI & Embedded Security SDK](https://github.com/maika-leehay/cyber-physical-robotics-sdk)
Modular 15-subsystem C++17, ROS 2, OpenSCAD, and Python suite validated via deterministic Hardware-in-the-Loop (HIL) benchmarks:

| Domain | Verified Subsystem Module | Key Engineering Benchmark |
| :--- | :--- | :--- |
| **Embedded Controls** | [`firmware/imu-kalman-filter-mpu6050`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/firmware/imu-kalman-filter-mpu6050) | **92.3% orientation RMSE reduction** (`10.53°` to `0.81°`) @ 200 Hz with thermal gyro bias tracking |
| **RTOS & Fieldbus** | [`firmware/freertos-socketcan-pid-controller`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/firmware/freertos-socketcan-pid-controller) | **1 kHz FreeRTOS anti-windup PID** (`< 0.01°` error, `82 ms` disturbance recovery) over SocketCAN |
| **ROS 2 Autonomy** | [`ros2_ws/src/amr_description_nav2`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/ros2_ws/src/amr_description_nav2) | Parametric URDF/Xacro inertia tensors, **RK2 midpoint arc odometry**, and 3-sector LiDAR avoidance |
| **Mechanical CAD** | [`hardware_cad/parametric-sensor-enclosure`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/hardware_cad/parametric-sensor-enclosure) | OpenSCAD assembly + C++17 **1.67% snap-fit strain** (`1.32x` PETG safety factor) & `+10.14 °C` thermal check |
| **Robot Learning** | [`control_learning/mujoco-lerobot-act-policy`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/control_learning/mujoco-lerobot-act-policy) | **61.4% Sim-to-Real RMSE reduction** (`9.52 mm` to `3.67 mm`) via domain randomization & `k=16` ACT |
| **Edge AI Vision** | [`perception/onnx-ros2-vision-node`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/perception/onnx-ros2-vision-node) | IoU Non-Maximum Suppression & RGB-D pinhole camera back-projection to metric 3D grasp poses |
| **Predictive Maint.** | [`perception/predictive-maintenance-anomaly-detector`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/perception/predictive-maintenance-anomaly-detector) | Early ball-bearing spalling isolation via **Peak-to-RMS Crest Factor** & Mahalanobis scoring |
| **Gesture Teleop** | [`perception/gesture-teleop-ros2-streamer`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/perception/gesture-teleop-ros2-streamer) | 21-point MediaPipe hand-landmark ROS 2 Twist mapper with tremor deadzone & `150 ms` watchdog |
| **CAN Bus Security** | [`security/socketcan-ids-iso21434`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/socketcan-ids-iso21434) | **ISO/SAE 21434** timing IDS, monotonic anti-replay counter & **AUTOSAR SecOC** 16-bit Keyed-MAC |
| **ROS 2 Hardening** | [`security/sros2-dds-enclaves`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/sros2-dds-enclaves) | **SROS2 / OMG DDS-Security** X.509 PKI enclaves & AES-256-GCM XML topic access governance |
| **Secure Boot OTA** | [`security/mcuboot-ota-rollback-verifier`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/mcuboot-ota-rollback-verifier) | **MCUboot (`0x96F3B83D`)** dual-slot A/B ECDSA verification, OTP SVN anti-rollback & watchdog revert |
| **AEAD Telemetry** | [`security/mqtt-aes-gcm-telemetry-node`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/mqtt-aes-gcm-telemetry-node) | Encrypted edge-to-cloud MQTT framing with 64-bit monotonic IV nonces & Verify-Then-Decrypt MAC |
| **Adversarial ML** | [`security/adversarial-vision-patch-defense`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/adversarial-vision-patch-defense) | FGSM attack generator, L1 Feature Squeezing & cross-modal LiDAR/stereo depth spoof detection |
| **EU CRA & SBOM** | [`security/cra-firmaudit-sbom-scanner`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/cra-firmaudit-sbom-scanner) | Automated **EU Cyber Resilience Act (EU 2024/2847)** CWE-120/798 SAST, MCUboot & **CycloneDX 1.5 SBOM** |
| **AI Safety Watchdog** | [`security/hardened-ai-policy-safety-interlock`](https://github.com/maika-leehay/cyber-physical-robotics-sdk/tree/main/security/hardened-ai-policy-safety-interlock) | **CVE-2026-25874** Pickle RCE guard, Kalman FDI residual filter & **ISO 10218-1:2025** standstill interlock |

### 2. [NutriSnap AI: Smart Canteen IoT Scale & Multimodal Nutrition Platform](https://github.com/maika-leehay/nutrisnap-ai)
* **Hardware-to-Cloud Architecture**: Custom **ESP32 + HX711 24-bit load-cell firmware** (`esp32_hx711_scale_bridge.ino`) streaming 5 Hz calibrated mass telemetry over Web Serial/UART to a containerized **FastAPI / SpringBoot / Docker** backend.
* **Competition Recognition**: Official entry (#528775) in the **2026 14th National College Digital Media Science & Technology Competition**.

## Contact & Engineering Inquiries
* **Email**: [abdelmounaimmekaoui@gmail.com](mailto:abdelmounaimmekaoui@gmail.com)
