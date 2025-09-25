# AI-Optimized-UAV-Navigation-in-Jamming-Environments-
A Sustainable Solution for Defense and Civilian SAR.

# sim-uav-fallback
Project: UAV GNSS-fallback simulator (student project)

## Mục tiêu
Demo pipeline: Detector (GPS-health) → Mode switch → VO (VINS/ORB) + IMU EKF fusion → waypoint controller.

## Cách chạy (mô phỏng)
1. Cài dependencies: `pip install -r requirements.txt`
2. Chạy simulator (AirSim/Gazebo) theo hướng dẫn trong `/sim_setup/README.md`
3. Launch ROS nodes:
   ```bash
   roslaunch ros_nodes ekf_fusion.launch
   python3 ros_nodes/detector_node.py


********Mẫu checklist kỹ thuật (cho nhóm thực hiện)********

 Cài Gazebo hoặc AirSim + ROS (chọn 1).

 Tạo dataset mô phỏng: camera+IMU logs, GNSS quality label (good/bad) hoặc giả lập giảm SNR.

 Triển khai detector (CNN nhỏ) hoặc heuristic trên RSSI/SNR (baseline).

 Cài VINS-Mono / ORB-SLAM2 và kiểm thử trên logs.

 Viết node ROS tích hợp: khi detector báo "GNSS bad" → publish mode = VO.

 Kịch bản sim: waypoint mission + inject GNSS-loss event; thu logs.

 Chạy 10+ thử nghiệm, thu metric; làm bảng kết quả.

 Chuẩn bị báo cáo, slide & demo video (3–5 phút).
