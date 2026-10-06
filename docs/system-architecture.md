# System Architecture

## 1. Architecture Overview

The AI Smart Manufacturing Cell is an intelligent automated manufacturing system that combines mechanical design, robotics, computer vision, artificial intelligence, and industrial automation.

The system is organized into several interconnected subsystems that work together to detect, inspect, classify, and sort manufactured parts.

## 2. High-Level System Flow

```text
                 ┌─────────────────┐
                 │   Input Parts   │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │    Conveyor     │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Presence Sensor │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │     Camera      │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Computer Vision │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │   AI Inspection │
                 └────────┬────────┘
                          │
                 ┌────────┴────────┐
                 │                 │
              GOOD              DEFECT
                 │                 │
                 ▼                 ▼
          ┌─────────────┐   ┌─────────────┐
          │    Robot    │   │    Robot    │
          └──────┬──────┘   └──────┬──────┘
                 │                 │
                 ▼                 ▼
            Good Bin          Defect Bin
3. Mechanical Layer
The mechanical layer contains the physical structure of the manufacturing cell.
Main components:
- Structural frame
- Conveyor system
- Product holders
- Robot mounting structure
- Camera mounting structure
- Good-part container
- Defective-part container
The mechanical components will be designed using CAD software.
4. Sensing Layer
Sensors provide information about the physical state of the manufacturing cell.
Initial sensors:
- Part presence sensor
- Conveyor position sensor
- Robot position feedback
- Emergency stop input
Future sensors may include:
- Temperature sensors
- Vibration sensors
- Current sensors
- Force sensors
5. Control Layer
The control layer coordinates the physical components of the manufacturing cell.
Main responsibilities:
- Conveyor control
- Sensor processing
- Robot commands
- System sequencing
- Emergency handling
- Communication between subsystems
The prototype may use a microcontroller or PLC for system control.
6. Computer Vision Layer
The computer vision system receives images from the inspection camera.
The processing pipeline is:Camera
   ↓
Image Acquisition
   ↓
Image Preprocessing
   ↓
Object Detection
   ↓
Feature Extraction
   ↓
AI Classification
The computer vision subsystem will initially use OpenCV for image processing.
7. Artificial Intelligence Layer
The AI system analyzes the captured images and determines the quality state of each manufactured part.
Initial classification:
GOOD
DEFECTIVE

Future versions may classify specific defect types, including:
- Surface defects
- Cracks
- Dimensional defects
- Missing components
- Incorrect orientation
The AI model will be evaluated using standard machine learning metrics such as accuracy, precision, recall, and F1-score.
8. Robotics Layer
The robotic system performs automated part handling and sorting.
Main operations:
- Pick part
- Move part
- Place part
- Sort part
The robot receives the inspection result from the AI system and performs the appropriate sorting action.
9. Data Layer
The system will store manufacturing and inspection information.
Example data:
- Part ID
- Timestamp
- Classification result
- Defect type
- Processing time
- Robot status
- Conveyor status
The stored data can later be used for production analysis and optimization.
10. Monitoring Layer
A real-time dashboard will provide information about the manufacturing cell.
The dashboard will display:
- Total production
- Good parts
- Defective parts
- Defect rate
- System status
- Robot status
- Conveyor status
- Camera status
11. Communication Architecture
The subsystems will communicate through defined interfaces.
The general communication flow is:
Sensors
   ↓
Controller
   ↓
Computer / AI System
   ↓
Robot Controller
   ↓
Actuators

Production and inspection data will also be sent to the monitoring system.
12. Safety Layer
Safety will be considered throughout the system design.
Initial safety mechanisms:
- Emergency stop
- Motor shutdown
- Robot stop command
- Safe operating boundaries
- Fault detection
- System status monitoring
The physical prototype will require additional safety validation before autonomous operation.
13. Future Extensions
The architecture is designed to support future capabilities such as:
- Digital Twin
- Predictive Maintenance
- Production Optimization
- Energy Monitoring
- Advanced Defect Detection
- Autonomous Process Optimization
- Multiple robotic stations
- Multi-class defect classification
