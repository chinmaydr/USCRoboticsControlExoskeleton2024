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
   - **One of the best knee exoskeleton models is from the [Neurobionics lab at the University of Michigan](https://neurobionics.robotics.umich.edu/research/wearable-robotics/knee-exoskeleton/)**
     - **Most other approaches to this use different actuator designs, making our method somewhat unique for the knee actuator**
     - **Cambridge University had [another model](https://www.cambridge.org/core/journals/wearable-technologies/article/serieselastic-actuator-with-two-degreeoffreedom-pid-control-improves-torque-control-in-a-powered-knee-exoskeleton/FBEBF3966808F9AC51138792D3B6BF10) which was similar but had the SEA in front of the knee, which requires more force than our approach as there is a smaller distance between the force and pivot.**

![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/903ffb2c-4737-46c9-9417-23c9c3532ff3)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/8ffe1dfa-c2bf-4315-b0eb-85c23f3e5e32)

## Approach
- **Technical Details:**
  - **Focused on knee**
  - **Used a single axis rotational movement**
    - **Forward up and down**
    - **Human walking is very dynamic, but we've simplified the knee to its major axis of rotation**
  - **Human leg simulation**
    - **Used Matlab**
    - **2 link robot acting as human legs**
  - **Simple exoskeleton**
    - **An Assistive device with series elastic actuator (SEA with spring and motor)**

![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/abb2d030-0106-4e43-b6a1-8889d0a8a792)

- **Technical Contributions:**
  - **Added mass to human model**
    - **Simulated human load/weight**
  - **No torque on knee joint**
    - **Motor 2 is knee joint**
    - **No torque represents weaken or nonfunctional knee**
  - **PD/PID controls**
    - **Used SEA/exoskeleton**
    - **More control**
  - **Exoskeleton worked**
    - **Supported load**
    - **Moved weakened knee**
  -  **Simulation and exoskeleton results**
    - **Contribute to science and wearable robotics**
    - **Expand to other joints (hip, ankle, etc.)**
    - **Allow researchers and companies to use results for their works**
 
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/234856ff-8858-4d00-8a78-4a3022bcb873)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/56d7b7a6-5052-4066-bf2a-8013c8454c30)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/e12c7186-e8cf-4f69-a100-bf045f226bfc)

## Models and Results
- **Stage 1: Initial Leg model with moving knee joint**
  - **Modified from model provided by mentors**
  - **No major issues, just learning how to use simulink**
  - **Leg continuously rapidly shakes back and forth due to the lack of a damping coefficient**
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/6c919f2d-2a5b-4708-85e8-231c5deb564b)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/b33c321c-53a5-4d1a-9d52-94aeb68ad150)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/ddd142ec-3028-4488-be7d-5a351c34a5bd)
<video src="videos/baselegmoving.mp4" width="320" height="240" controls></video>
- **Stage 2: Initial Leg model with moving knee joint attached to ground. Torque added to joints to make it stand**
  - **Initially made it fall due to gravity, then added torque**
  - **Issues faced(and resolved)**
    - **Anchoring - Used transformations to make it bend the right way**
    - **Leg was too heavy - Made it lighter**
    - **Learned about spatial contact force to make it act like a real leg wihtout solids phasing through each other**
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/d71e78a8-0d37-4c04-96a3-bcf8ac055521)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/9f2cce30-5e40-4e86-81a5-4309d77a4389)
<video src="videos/legsitting.mp4" width="320" height="240" controls></video>
<video src="videos/legstanding.mp4" width="320" height="240" controls></video>

## Conclusion
- **Learned core robotics concepts**
  - **Modeling with Matlab / Simulink / Simscape**
  - **Understanding PD (and PID) control**
- **Advantages and problems of current exoskeleton ideas**
  - **Advantages and problems with robots with springs and compliant materials**
- **Learned basics of research and paper review**
- **Designed a mechanism and produced results**
- **Project can be used by research and companies designing safe wearable exoskeletons for the disabled**

![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/78b229b4-ef63-46cf-b7c7-e7a3c7f2af21)

## Future Work
- **Matlab simulation**
  - **More realistic human model**
  - **Advanced exoskeleton**
- **Full lower half exoskeleton**
  - **Hip, knee, and ankle**
  - **More rotational movement**
- **Prototype/Real Device**
  - **Comfortable**
  - **Safe**
  - **Affordable**
  - **Energy Efficient**
  - **Lightweight**
  - **Strong**
- **Spread to researchers and companies**

![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/b1ef7e85-d0e3-492f-b23f-f7ab85d707c0)
![image](https://github.com/chinmaydr/USCRoboticsControlExoskeleton2024/assets/68085673/564d7c0f-bb6f-40db-afdf-1e44fc07c422)
