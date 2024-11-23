# Moveit
## 사전 진행
> [참고] https://moveit.picknik.ai/humble/doc/how_to_guides/how_to_generate_api_doxygen_locally.html
<br/> 
1. 실행 <br/> 
   - ros2 launch moveit2_tutorials demo.launch.py rviz_config:=panda_moveit_config_demo_empty.rviz

![Screenshot from 2024-11-23 14-24-27](https://github.com/user-attachments/assets/0ca170b1-7c3e-4e24-947f-893ea1bad006)
<br/> 
2. rviz화면
   - Add - moveit_ros_visualization 폴더에서 DisplayType으로 “MotionPlanning”을 선택
   - RViz에서 Panda 로봇을 볼 수 있음
   - 모션 플래닝 플러그인을 로드 -> 구성 시작
   - "디스플레이" 하위 창의 "전역 옵션" 탭에서 고정 프레임 필드를 다음과 같이 설정합니다. [/panda_link0]
   - "디스플레이" 내에서 "MotionPlanning" - Robot Description : robot_description.
   - Planning Scene Topic : /monitored_planning_scene
   - Planned PAth : ./display_planned_path
   - Planning Request : Planning Group => panda_arm으로 변경
   - 왼쪽 하단의 MotionPlanning 패널에서도 이를 확인 가능

![Screenshot from 2024-11-23 18-22-17](https://github.com/user-attachments/assets/3008e64c-4c52-4a84-9408-5786fb6a3705)

