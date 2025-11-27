Rockfall Detection and Monitoring System

A GNN-based 3D monitoring system designed to analyze terrain stress points, process sensor CSV data, simulate rockfall risk on a 3D mesh, and trigger alerts based on region-wise employee mapping. The system aims to provide a simple, practical solution for industries such as mining, construction, and tunneling operations.

1. Overview

This project focuses on real-time rockfall risk visualization using:

3D terrain models

Sensor CSV inputs

Color-coded node risk calculation

Region-based alert mapping

Employee management

Real-time monitoring dashboard

Simulation tools

Blast Simulations

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

<img width="1920" height="1080" alt="realtime monitoring" src="https://github.com/user-attachments/assets/1a69a4ad-2fd0-42e9-9f69-7a37f7e747fd" />


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




4. Simulation Module

The simulation page provides an interactive 3D environment:

Rotate, move, zoom inside the terrain

Click any node to open a Node Info window

View complete node parameters

Shows exact risk percentage

Adjust sensor values manually (+ / – buttons)

System recalculates node risk in real time

Drag & place tools (e.g., dynamite effects) available on the UI

<img width="1920" height="1080" alt="simulation" src="https://github.com/user-attachments/assets/80aaebfe-e7a5-4c67-996b-bc12561dbb3f" />


5. Employee Management

The Employee Management module provides:

Add, Edit, Delete employees

Region assignment (Central, North, South, etc.)

Region-wise employee count

Department field

Automatic linking between region risk and employee responsible

<img width="1920" height="1080" alt="emp management " src="https://github.com/user-attachments/assets/7c32af4b-a23a-42ae-96e3-bbf6bf0949a1" />


6. Alert System

Risk alerts are generated automatically when:

Node risk exceeds threshold

Region associated with an employee is affected

Alert popup contains:

Risk percentage

Region name

Employee name

<img width="1920" height="1080" alt="system" src="https://github.com/user-attachments/assets/df67314c-b74a-4941-971c-01f82d52b047" />  ![alert call](https://github.com/user-attachments/assets/e404523a-a2fa-4e4f-a940-a7a9b66b1190)

7. Risk Score Calculation

Risk scoring is done through a simple threshold-based formula using:

Temperature

Humidity

Ground pressure

Vibration

Crack width

Rainfall

Red nodes represent highest stress, yellow moderate, blue low.

This system does not use AI. All logic is deterministic.

8. File Inputs
3D Model

Supports formats like OBJ, GLB, STL.

Sensor CSV

Example columns:

node_id,temperature,humidity,ground_pressure,vibration,crack_width,rainfall

9. Technologies Used

Python

PyQt6

OpenGL (for 3D rendering)

CSV processing

JSON/local DB for employee storage

Standard threshold-based risk logic

10. Limitations

No GNN or ML model yet

Risk fully depends on rule-based scoring

3D model must be pre-cleaned

Desktop-only application

CSV must contain clean sensor values

11. Future Improvements

Integrate GNN/ML-based rockfall prediction

Real-time IoT-based sensor ingestion

SMS / WhatsApp / automated call alert APIs

Physics-based simulation

Cloud dashboard with multi-user support
