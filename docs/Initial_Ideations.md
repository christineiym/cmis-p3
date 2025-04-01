# Initial Ideation

## Gesture-Controlled Origami Frog

### Utility

- **Motivation**  
  This project explores playful and personalized physical interaction through a gesture-controlled origami frog. It offers a stress-relieving and engaging experience while showcasing real-time mechanical motion integration.

- **Use Context**  
  Designed for everyday users as an interactive desk toy or conversation piece. The frog is controlled using wrist-worn IMU-based gestures, ensuring intuitive and accessible interaction.

- **Personalization & Customization**  
  The frog’s hopping behavior is optimized based on user-defined motion parameters such as hop angle, height, and motor power. Custom fabrication allows the mechanical skeleton to adapt to user preferences and constraints like motor torque, material properties, and size.

- **In-Class Showcase**  
  During the live demo, the frog will be triggered via IMU gesture input. The inverse design tool will demonstrate how the geometry updates in real-time based on user-defined parameters.

### Optimization

- **User Input**
  - Desired hop height or motion trajectory  
  - Physical constraints such as actuator torque  
  - Bounding box size for printable structure and origami wrapping

- **Mathematical Representation**  
  - Decision variables include linkage lengths, joint angles, and pivot locations
  - Geometry represented via parametric sketches or mesh primitives

- **Objective**  
  - Maximize vertical displacement (hop height) while respecting physical and material constraints

- **Constraints**  
  - Hard: Printer volume, motor torque, material limits, origami compatibility
  - Soft: Hop smoothness, motion cycle time

- **Optimizer & Tools**  
  - Use Simulated Annealing or COBYLA via `scipy.optimize`  
  - Geometry generation via `cadquery` or `trimesh`, exportable as STL

- **In-Class Showcase**  
  - The UI takes user-defined inputs and runs optimization under 2 minutes
  - Generates updated 3D printable skeleton and visual output

### Fabrication

- **Pipeline**  
  - Print 3 optimized frog skeletons using PLA  
  - Wrap each with paper-folded origami skin  
  - Embed motor for actuation; controlled by Arduino Nano 33 BLE Rev2 and battery

- **Programming Languages**  
  - Python: Optimization pipeline and BLE communication  
  - C++: Arduino firmware for motor actuation

- **In-Class Showcase**  
  - Demonstrate 3 physical frog versions  
  - Users interact via wearable IMU, triggering gesture-driven hopping behavior