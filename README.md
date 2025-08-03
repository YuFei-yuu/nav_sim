# 食用方式

## 建图
- 启动仿真
    ```bash
    ros2 launch pb_rm_simulation rm_simulation.launch.py
    ```
- 启动建图
    ```bash
    ros2 launch sentry_bringup mapping.launch.py 
    ```
- 启用键盘控制
    ```bash
    ros2 run teleop_twist_keyboard teleop_twist_keyboard
    ```
- 存储地图
    ```bash
    ros2 run nav2_map_server map_saver_cli -t /projected_map -f test_map --fmt png
    ros2 service call /map_save std_srvs/srv/Trigger
    ```

## 重定位
- 启动仿真
    ```bash
    ros2 launch pb_rm_simulation rm_simulation.launch.py
    ```
- 启动重定位
    ```bash
    ros2 launch sentry_bringup bringup_all_in_one.launch.py
    ```

## 决策
- 启动模拟裁判系统
    ```bash
    ros2 run control_panel control_panel
    ```
- 启动决策
    ```bash
    ros2 launch rm_decision_cpp run.launch.py
    ```