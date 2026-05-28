# 🤖 Vision-Based Robot Arm Dynamic Control

스마트폰 카메라와 OpenCV를 활용하여 객체를 실시간으로 탐지하고, 로봇팔이 해당 위치로 이동하도록 물리적 좌표를 매핑하는 동적 제어(Dynamic Control) 시스템 실습 프로젝트입니다.

> 💡 **Reference & Contribution**
> 본 프로젝트의 코어 모션 제어 코드(Core Algorithm)는 창업동아리 '미래제품연구회' 교육팀장에 의해 작성되었습니다. 저는 해당 코드를 기반으로 **하드웨어 키트 조립, ESP32 구동 환경 구축, 기초 CAD 모델링, 그리고 비전(OpenCV) 데이터와 액추에이터를 연동하는 시스템 통합(System Integration) 및 실구동 테스트**를 주도적으로 수행하였습니다.

## 🛠 Tech Stack
* **Hardware:** ESP32, 3-DOF Robot Arm Kit, Smartphone Camera
* **Software:** `Python 3`, `OpenCV`, `MicroPython (Thonny)`, `Fusion 360`, `VS Code`

## ⚙️ System Workflow & My Role

### 1. Hardware & Basic Setup
* 로봇팔 하드웨어 키트(3-DOF) 직접 조립 및 배선.
* ESP32 마이크로컨트롤러 환경 구성 및 PC 통신 인터페이스(Serial) 세팅.

### 2. CAD Modeling (Fusion 360)
* Fusion 360을 이용한 기초 3D CAD 모델링 실습.
* 하드웨어 설계 데이터의 물리적 제약사항(가동 범위, 간섭 등)에 대한 이해도 향상.

### 3. Actuator Control (MicroPython)
* Thonny IDE를 활용하여 서보모터 구동 테스트.
* 각 관절(Joint)의 각도 제어를 위한 MicroPython 스크립트 실행 및 하드웨어 캘리브레이션(Calibration) 수행.

### 4. Vision Integration (OpenCV)
* VS Code 환경에서 OpenCV를 이용해 스마트폰 카메라(IP Webcam) 영상 데이터 실시간 수신.
* 영상 내 특정 객체를 탐지하고 2D 픽셀 좌표를 획득.

### 5. Dynamic Motion Control
* 추출된 픽셀 좌표를 로봇팔의 3D 물리적 공간 제어 좌표계로 매핑.
* 계산된 타겟 좌표 데이터를 ESP32로 전송하여, 외부 환경 변화에 따라 로봇팔이 실시간으로 목표 위치로 이동하는 피드백 제어 시스템 완성.

## 📷 시연 사진
<img width="1835" height="1002" alt="ArUCo 마커 탐지" src="https://github.com/user-attachments/assets/5d3d562d-a6d3-4078-9503-fa462712fbdf" />
<img width="1862" height="1019" alt="hsv 객체 탐지" src="https://github.com/user-attachments/assets/527af715-07a1-4a3f-b92a-3cbe51b688f6" />
<img width="1913" height="1080" alt="openCV 스마트폰 카메라 연동" src="https://github.com/user-attachments/assets/a801d79c-0ac9-4485-a09b-81302e2685ef" />
