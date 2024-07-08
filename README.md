# Using Series Elastic Actuators for Knee Exoskeletons
## Motivation
- **To provide aid to those without fully functioning knees to perform basic tasks**
  - **Elderly or disabled with non-funtioning or partially functioning knees**
    - **As a possible extension, it could also be used for soldiers or hikers who get tired walking long distances or carrying heavy loads**
  - **To aid in tasks like walking, kneeling, sitting, standing, or squatting**
  - **Make exoskeletons more safe and adaptable by using compliant mechanisms over rigid ones**
    - **Also more accessible to the general public as compliant mechanisms generally cost less**
    
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/0915ed6b-0bae-4145-8f19-95a4d10a421a)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/b79d4419-b2a7-4ff6-bd51-6f9ccfecaecb)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/cf899156-850e-4936-a44a-c9f3f438120a)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/7d48c660-527e-4dbc-adb0-b2764a51f379)

## Background
- **Flexsea-Execute: advanced motion controller for wearable robotic applications**
  - **Journal: MIT Media Lab Research-Publications: Biomechanics (July 8, 2016)**
  - **Objective: Provide advanced motion microcontrollers for robotic prosthetics To improve quality of life and obstacles of wearable robots**
  - **Using Flexible SEA instead of common motor to move lower limb exoskeleton**
  - **Communication software connects to nervous system signals tells FlexSEA how/when move**
  - **Similar to how human body bends and moves could be used to revolutionize exterior movement supports for humans**
  - **Used this Article as a baseline for how we could model our own simulation in Simulink**

![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/38e27264-8f81-4a6a-9ae5-c9a89449d337)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/fcc82fe2-6f39-4431-9a18-2a8f4ae26189)

- **Design of physical user–robot interactions for model identification of soft actuators on exoskeleton robots**
  - **Journal: The International Journal of Robotics Research**
  - **Objective: To accurately identify soft actuator models for wearable robots Successfully use physical robot interactions where a user applies external forces to the robot**
  - **Soft pliable actuators move exoskeleton > rigid stiff motors**
  - **More effective at mapping general human lower limb movements**
  - **GP active learning algorithm trained to determine robot trajectory**
  - **Generates Joint torques equal to humans and aids in walking**
  - **Used this Article’s baseline human walking tests to outline our own model**

 ![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/887f0166-4129-4fd5-a3d6-4a8ef2c00cf0)

 - **Other Research**
   - **One of the best knee exoskeleton models is from the Neurobionics lab at the University of Michigan**
     - **Most other approaches to this use different actuator designs, making our method somewhat unique for the knee actuator**
     - **Cambridge University had another model which was similar but had the SEA in front of the knee, which requires more force than our approach as there is a smaller distance between the force and pivot.**

![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/903ffb2c-4737-46c9-9417-23c9c3532ff3)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/8ffe1dfa-c2bf-4315-b0eb-85c23f3e5e32)

## Approach
## Models
## Control
## Results
## Future Work
