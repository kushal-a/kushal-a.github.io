---
title: "General Indoor Navigation oh Humanoid Robots"
excerpt: "Developing generalist policies for indoor navigation in humanoid and other legged systems<br/><img src='/images/legged_team.png'>"
collection: portfolio
---

We are developing a mobile manipulator platform capable of safe, reliable, and generalizable autonomy in human environments. The system will demonstrate full building-scale navigation and interaction—handling tasks such as operating elevators, opening doors, traversing staircases, and moving across multiple floors—without human intervention. 

## Technical Approach
### 3D Mapping & Localization:
- High-precision SLAM (fastlio2) and global local planning (3D A*, cmu_local_planner) for robust navigation in dynamic, cluttered spaces.
### Perception & Scene Understanding: 
- Fusion of LiDAR, RGB-D, and semantic models for reliable obstacle avoidance, spatial reasoning, and environment grounding.
### Manipulation Capabilities:
- Dexterous interaction with common infrastructure i.e. button pressing, door pushing/pulling, object placement.
### Locomotion Capabilities: 
- Reinforcement learning based control for robust and smooth locomotion on plane, rough terrain and stairs
- Capable of push-recovery and fall-recovery
### Learning & Adaptation:
- Reinforcement learning and imitation learning in simulation (Isaac Gym, MuJoCo)
- Policy transferred to hardware for real-world tasks.
### Agentic Autonomy:
- High-level task planning and skill composition, enabling long-horizon missions such as “navigate from office A to lab B across floors. Then grab me a coke from the kitchen on the second floor and bring it to me”
- Using VLM for general perception (segmenting elevator buttons, interacting with elevator panels)


More coming soon...