# Jump-up-Labs-TEMPLATE
# 국립한밭대학교 인공지능소프트웨어학과 Perceptional AI Robotics Learning LAB팀

**팀 구성**
- 20221044 김내경
- 20221047 김윤희
- 20221052 서민경
- 20221080 최진
- 20231050 김파란하늘
- 20231051 김현빈
- 20231052 김현정
- 20231068 이연서
  
## Project Background
- ROS2 기반 자율주행 로봇의 설계–개발–검증을 하나의 파이프라인으로 통합해 개발 비용·시간을 절감하고 반복 가능한 실험 환경을 확보하려는 프로젝트입니다.

- 초기 단계에서 Gazebo 시뮬레이터로 센서 융합, SLAM, 경로 계획을 안전하게 검증하고, 이후 TurtleBot 실기기로 이전(시뮬→실기기 전이)하여 자율주행을 완성합니다.

## System Model
- ROS2(노드/토픽/서비스/액션) 기반 모듈화. 시뮬레이터(Gazebo)–실기기(TurtleBot) 간 동일 인터페이스 유지.
- 시뮬레이션 계층(Gazebo): 로봇 모델·가상 센서·지도/환경 구성, SLAM·Nav2 사전 튜닝.

- 미들웨어 계층(ROS2): 노드/토픽/서비스/액션 기반 모듈화, 시뮬–실기기 공용 인터페이스.

- 자율주행 계층:

SLAM(Cartographer/RTAB-Map 중 택1), Navigation(Nav2) 전역/지역 플래너, 장애물 회피.

Perception: 카메라 탑재, 사람 Detection(YOLO 계열 가능).

- 조작 계층: 다관절 로봇팔 + MoveIt으로 간단 검사/픽업 시나리오 수행.

- 하드웨어 계층(TurtleBot): 모터·IMU·LiDAR/Depth 카메라(선택), SBC(ROS2 런타임).
## Numerical Results
- ABCD

## Conclusion
- Gazebo에서 SLAM/내비를 튜닝하고, 실주행에서 미세 조정하는 방식으로 시행착오를 크게 줄였다.
- ROS2 프로그래밍, 센서 데이터 처리, SLAM 및 경로 계획 알고리즘 튜닝을 하였다.
- 시뮬 먼저, 실기기 전이 전략으로 시행착오를 줄이고 튜닝 반복성을 확보했다.
- ROS2 모듈화 덕분에 이동·인지·조작을 단계적으로 붙여도 인터페이스가 유지되고 재사용이 쉽다.

## Project Outcome
- 기술적 성과
  ROS2 패키지 세트 구축- Bringup, SLAM, Nav2, Perception(YOLO), MoveIt 패키지 및 공통 런치/파라미터 템플릿 정리.
  Gazebo 월드/로봇 모델, TF 프레임 표준화, 센서 캘리브레이션 스크립트(imu/lidar/cam) 일괄화.
  
