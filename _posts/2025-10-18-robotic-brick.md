---
layout: post
title:  "Robotic Brick-Stacking Simulation"
hero: https://source.unsplash.com/collection/430471/
overlay: blue
published: true

---

# something about choice

Grasshopper plugin: Robots
Robotic Arm and settlement: AA Kuka KR30
Brick dimension: 
162mm x 44mm x 94mm

----

The robotic brick-stacking simulation is a self learning project, intends to summarize a distinct workflow on how to program, regulate and perform as a role of designer in the digital fabrication field. Due to lack of access with robotic arm in the real physical world, the process can only be demonstrated in the display. 

The Input of the designated brick wall is based on an arbitrary loft surface by 2 curves with inverted convex direction respectively. In order to extract the designated coordinates to be utilized for the tool path, contour lines were generated with the distance of the brick height. A proper distance division was accordingly conducted to get to the target plane. For each target coordinated plane being rotated consequently, the geometry was transmitted into coordinations through which we can be interactive with the machines.   

----

Despite the location of target plane, additional configurations require to be considered for the purpose such as signal interaction with end effectors, cautious placement to the location with lower velocity, or adequate motion configuration. Nevertheless, a digital signal input passing to the brick clipper is demanded as the brick being conveyed to the destination. 

----

The work environment settlement is also crucial preparation by utilizing the robotic arm in digital fabrication. Firstly, the choice of a suitable robotic arm because of the mechanism for the task will alleviate the later programming process for collision avoidance with toolhead and robot itself. For instance, the UR10 has less dimension between wrists and could frequently bring out collision, the motion planner has to constrain the joint angle on the wrist and yet shrink the reachable scope of workspace meanwhile. Additionally, the workspace should envelop the target plane perfectly with a "safety factor". Not all the target will be reachable if the coordination angle limits some rotation axis of the robot's joints, typically near the end effectors, as shown in the figures. There might be feasible solutions if more advanced motion planning modules imported in the programming step such as MoveIt in ROS, however as the first simulation it's out of the capability of this project. 

The picking and stacking process was conducted as loop whereas in grasshopper3D presented as tree branches. It is presumed that the initial picking point remains unchanged and the brick will firstly be lifted up then to a plane bit higher and close to the goal target. During these stages joint motions are employed for rapid and efficient movements. Slow and cautious lineal motions are adopted to release the brick to prevent potential collapse of the wall. Zoning areas are also applied for the sake of smooth movement for robot. The robots plugin can transfer the program into robot code such as RAPID or KRL. 