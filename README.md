## 사전 진행
> [참고] https://moveit.picknik.ai/humble/doc/how_to_guides/how_to_generate_api_doxygen_locally.html
<br/> 
1. 실행 <br/> 
   - ros2 launch moveit2_tutorials demo.launch.py rviz_config:=panda_moveit_config_demo_empty.rviz

![Screenshot from 2024-11-23 14-24-27](https://github.com/user-attachments/assets/0ca170b1-7c3e-4e24-947f-893ea1bad006)

<br/> 
2. rviz화면 <br/>
   - Add - moveit_ros_visualization 폴더에서 DisplayType으로 “MotionPlanning”을 선택 <br/>
   - RViz에서 Panda 로봇을 볼 수 있음 <br/>
   - 모션 플래닝 플러그인을 로드 -> 구성 시작 <br/>
   - "디스플레이" 하위 창의 "전역 옵션" 탭에서 고정 프레임 필드를 다음과 같이 설정합니다. [/panda_link0] <br/>
   - "디스플레이" 내에서 "MotionPlanning" - Robot Description : robot_description. <br/>
   - Planning Scene Topic : /monitored_planning_scene <br/>
   - Planned PAth : ./display_planned_path <br/>
   - Planning Request : Planning Group => panda_arm으로 변경 <br/>
   - 왼쪽 하단의 MotionPlanning 패널에서도 이를 확인 가능 

![Screenshot from 2024-11-23 18-22-17](https://github.com/user-attachments/assets/3008e64c-4c52-4a84-9408-5786fb6a3705)

<br/>
3. 움직이기 <br/>
   - 계획 환경 에서의 로봇 구성 /monitored_planning_scene(기본적으로 활성화됨) <br/>
   - 로봇의 계획된 경로(기본적으로 활성화됨) <br/>
   - 녹색: 동작 계획의 시작 상태(기본적으로 비활성화됨) <br/>
   - 주황색: 동작 계획의 목표 상태(기본적으로 활성화됨) <br/>
<br/>
   - Scene Geometry : 로봇 시각적 표시 확인란을 사용하여 장면 로봇을 계획 <br/>
   - Planned Path : 로봇 시각적 표시 확인란을 사용하여 계획된 경로 확인 <br/>
   - Planning Request : 쿼리 시작 상태 체크 박스를 사용하여 시작 상태를 확인 <br/>
   - Planning Request : 목표 상태 쿼리 체크박스를 사용하여 목표 상태를 확인 <br/>

![Screenshot from 2024-11-23 18-24-18](https://github.com/user-attachments/assets/d173013e-ce7b-4c6b-9d07-d3a718429aa0)
