Rockfall Detection and Monitoring System

A desktop-based 3D monitoring system designed to analyze terrain stress points, process sensor CSV data, simulate rockfall risk on a 3D mesh, and trigger alerts based on region-wise employee mapping. The system aims to provide a simple, practical solution for industries such as mining, construction, and tunneling operations.

1. Overview

This project focuses on real-time rockfall risk visualization using:

3D terrain models

Sensor CSV inputs

Color-coded node risk calculation

Region-based alert mapping

Employee management

Real-time monitoring dashboard

Simulation tools

Automatic alert popups

Optional emergency call workflow

The system is fully rule-based and does not use ML or GNN models in the current version.

2. Real-time Monitoring

The Real-time Monitoring module allows users to:

Upload a 3D model of the terrain

Upload a sensor CSV file

Analyze stress points on the 3D surface

View color-coded risk levels for each node

Check environmental parameters through side meters

Monitor timestamps during live analysis

Screenshot
![Real-time Monitoring](images/realtime_monitoring.png)

3. Stress Analysis

The stress analysis workflow includes:

Upload 3D model

Upload sensor CSV

Generate stress/risk map

Display overall risk meter

Highlight critical nodes in red

Show detailed environmental readings including:

Temperature

Humidity

Ground pressure

Vibration

Crack width

Rainfall

Screenshot
![Stress Analysis](images/stress_analysis.png)

4. Simulation Module

The simulation page provides an interactive 3D environment:

Rotate, move, zoom inside the terrain

Click any node to open a Node Info window

View complete node parameters

Shows exact risk percentage

Adjust sensor values manually (+ / – buttons)

System recalculates node risk in real time

Drag & place tools (e.g., dynamite effects) available on the UI

Screenshot
![Simulation Module](images/simulation.png)

5. Employee Management

The Employee Management module provides:

Add, Edit, Delete employees

Region assignment (Central, North, South, etc.)

Region-wise employee count

Department field

Automatic linking between region risk and employee responsible

Screenshot
![Employee Management](images/employee_management.png)

6. Alert System

Risk alerts are generated automatically when:

Node risk exceeds threshold

Region associated with an employee is affected

Alert popup contains:

Risk percentage

Region name

Employee name

Screenshot
![Alert Popup](images/alert_popup.png)

7. Emergency Call Workflow

As part of the alert pipeline, the system can optionally trigger an emergency call sequence (manual or API-based).

Screenshot
![Emergency Call](images/emergency_call.png)

8. Risk Score Calculation

Risk scoring is done through a simple threshold-based formula using:

Temperature

Humidity

Ground pressure

Vibration

Crack width

Rainfall

Red nodes represent highest stress, yellow moderate, blue low.

This system does not use AI. All logic is deterministic.

9. File Inputs
3D Model

Supports formats like OBJ, GLB, STL.

Sensor CSV

Example columns:

node_id,temperature,humidity,ground_pressure,vibration,crack_width,rainfall

10. Technologies Used

Python

PyQt5

OpenGL (for 3D rendering)

CSV processing

JSON/local DB for employee storage

Standard threshold-based risk logic

11. Limitations

No GNN or ML model yet

Risk fully depends on rule-based scoring

3D model must be pre-cleaned

Desktop-only application

CSV must contain clean sensor values

12. Future Improvements

Integrate GNN/ML-based rockfall prediction

Real-time IoT-based sensor ingestion

SMS / WhatsApp / automated call alert APIs

Physics-based simulation

Cloud dashboard with multi-user support
