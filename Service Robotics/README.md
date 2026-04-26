# Service Robotics

A robotic project course at LTH. It involved designing and building a mobile rescue robot capable of navigating a maze, locating targets, and retrieving "victims" (wooden cylinders). 

## Breakdown of the project sections

### Physical design

- **Gripper and claw**: 3D-printed gripper with a claw and housing.

| Gripper |
| :---: |
| <img width="300" src="https://github.com/user-attachments/assets/4c312297-a93a-47ec-9816-3cfff08f758d" /> |


- **Robot housing**: Laser-cutted MDF housing.


| Robot housing |
| :---: |
| <img width="300" src="https://github.com/user-attachments/assets/1d9bc6e9-9e0f-4dc0-b18c-e55e1286bec6" /> |

### Electronics design

- **Actuators:** Two DC motors for steering and two servo motors for the claw rescue procedure (grabbing and lifting the wooden cylinders).
- **Sensors:** A front-mounted IR reflectance sensor for line following and a pressure sensor for determining when to grab the wooden cylinders. 
- **Power Management:** A high-capacity battery pack for the motors and a separate power bank for the microcontroller and sensors, to prevent voltage drops during high motor load.
  
### Algorithm design / Code

- **BFS(Breadth-First Search):** Used a BFS algorithm in order to find the shortest path (with respect to the number of nodes) from a map of the maze.
- **Adjacency Matrix:** Managed the intersections and turns of the maze in a 2D vector, to keep track of the current position and the most logical course.
- **Command Stack:** The algorithm has a pre-calculated stack of commands that the robot executes upon detecting a node with its IR sensors.

### Results

- Successfully retrieved all 3 victims during the final demo, at a navigation time of 1:52 minutes (208 points). 
  
| Short gif of final demo |
| :---: |
| <img width="450" src="https://github.com/user-attachments/assets/c3b8dc97-f4f9-4688-94ac-969af4fd6056" /> |





  
