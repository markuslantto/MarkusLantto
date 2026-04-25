# Service Robotics

A robotic-focused project course at LTH. It involved designing and building a mobile rescue robot capable of navigating a maze, locating targets, and retrieving "victims" (wooden cylinders). 

## Breakdown of the project sections

### Physical design

- **Gripper and claw**: 3D-printed gripper with a claw and housing.

| Gripper |
| :---: |
| <img width="300" src="https://github.com/user-attachments/assets/4c312297-a93a-47ec-9816-3cfff08f758d" /> |

https://github.com/user-attachments/assets/4c312297-a93a-47ec-9816-3cfff08f758d
<img width="1536" height="2048" alt="claw" src="" />

- **Robot housing**: Laser-cutted MDF housing. <img width="1536" height="2048" alt="rescuerobot" src="" />


| Robot housing |
| :---: |
| <img width="300" src="https://github.com/user-attachments/assets/1d9bc6e9-9e0f-4dc0-b18c-e55e1286bec6" /> |

### Electronics design

- **Actuators:** Two DC motors for steering and two servo motors for the claw operation (grabbing and lifting).
- **Sensors:** A front-mounted IR reflectance sensor for line following and a pressure sensor for determining when to grab the wooden cylinders. 
- **Power Management:** A high-capacity battery pack for the motors and a seperate power bank for the microcontroller and sensors, to prevent voltage drops during high motor load.
  
### Algorithm design / Code
