# Design Decisions

## 1. Project Scope

The first prototype will focus on automated quality inspection and robotic sorting of small manufactured parts.

The system will be developed incrementally, starting with simulation and software validation before physical hardware integration.

## 2. Product Selection

The initial product will be a small cylindrical mechanical part.

Target dimensions:

- Diameter: 30 mm
- Height: 20 mm
- Approximate mass: 30–50 g
- Material: Plastic or aluminum

The dimensions may be modified during the mechanical design phase.

## 3. Conveyor-Based Material Handling

A conveyor system will be used to transport parts between stations.

The conveyor provides:

- Controlled part movement
- Repeatable positioning
- Continuous material flow
- Easy integration with sensors and cameras

## 4. Camera-Based Inspection

A camera will be positioned above the inspection area.

This configuration was selected because it provides a relatively stable and repeatable view of the manufactured parts.

The camera system will initially focus on detecting visible defects and incorrect part conditions.

## 5. AI-Based Inspection

Artificial intelligence will be used to classify parts as GOOD or DEFECTIVE.

The AI inspection system will initially use a computer vision pipeline and will later be upgraded to a trained deep learning model.

This incremental approach reduces development complexity while allowing the system to evolve toward more advanced inspection capabilities.

## 6. Robotic Sorting

A robotic arm will be used to move inspected parts into the appropriate output location.

The robot will receive the classification result from the inspection system and execute the corresponding sorting operation.

## 7. Simulation Before Hardware

The system will be simulated before building the physical prototype.

Simulation will be used to validate:

- Mechanical layout
- Robot movement
- Conveyor workflow
- Sensor logic
- Inspection sequence
- Collision risks

This reduces hardware cost and allows design problems to be identified early.

## 8. Modular Architecture

The system will be divided into independent subsystems:

- Mechanical
- Sensing
- Control
- Computer Vision
- AI
- Robotics
- Monitoring

A modular architecture makes the system easier to test, debug, modify, and expand.

## 9. Software Strategy

Python will be used for:

- Computer vision
- AI development
- Data processing
- Backend services
- Testing

C++ may be used where performance or robotics integration requires it.

## 10. Version Control

Git and GitHub will be used throughout the project.

Development will be organized into meaningful commits and documented milestones.

The repository will contain:

- Source code
- CAD-related documentation
- Simulation files
- AI models
- Test results
- Technical documentation

## 11. Safety

Safety will be considered from the beginning of the design.

The system will include an emergency stop concept and controlled shutdown procedures.

Physical testing will only be performed after appropriate mechanical and electrical safety checks.

## 12. Development Strategy

Development will follow an incremental approach:

```text
Requirements
     ↓
System Architecture
     ↓
Mechanical Design
     ↓
Simulation
     ↓
Basic Automation
     ↓
Computer Vision
     ↓
AI Inspection
     ↓
Robot Integration
     ↓
Dashboard
     ↓
Testing
13. Future Expansion
The system is designed to support future features including:
- Digital Twin
- Predictive Maintenance
- Energy Monitoring
- Production Optimization
- Advanced Defect Classification
- Multiple robotic stations
- Autonomous process optimization
