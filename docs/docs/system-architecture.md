# System Architecture

## 1. Architecture Overview

The AI Smart Manufacturing Cell is organized into several interconnected subsystems.

The main architecture consists of:

- Mechanical System
- Sensing System
- Control System
- Computer Vision System
- AI Inspection System
- Robotic System
- Data and Monitoring System

## 2. High-Level Data Flow

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
