# BottleFill-ControlUnit

## Overview
BottleFill-ControlUnit is a SCADA-based automated bottle filling system developed using **Wonderware InTouch 10**. It is designed to streamline the industrial bottle filling process in sectors such as beverages, pharmaceuticals, and chemicals. This system allows real-time monitoring and control, reduces manual errors, and enhances operational safety and efficiency.

## Key Features
- SCADA-based monitoring and control using Wonderware InTouch 10
- Real-time visualization of bottle detection and fill status
- Start/Stop and emergency stop control via HMI
- Overflow detection and alarm handling
- Accurate fill control with timer/sensor-based logic
- Scalable and easily integrable with PLC systems

## Technologies Used
- **SCADA Software**: Wonderware InTouch 10
- **HMI Platform**: WindowMaker / WindowViewer
- **Communication**: Direct I/O or OPC/DA (with PLCs)
- **Controllers**: Compatible with soft PLCs or physical PLCs (e.g., Allen-Bradley, Siemens)
- **Sensors**: IR sensor for bottle detection, optional level sensor
- **Actuators**: Solenoid valves, optional conveyor motor

## System Workflow
1. Bottle presence is detected via sensor
2. Solenoid valve opens to fill bottle
3. After a defined time or level detection, the valve closes
4. The system updates the count and status on the HMI
5. Alarms are triggered for overflow or absence of bottle
6. Operators can control the system via touch interface

## Installation and Setup

### 1. Restore InTouch Application
- Open **InTouch Application Manager**
- Go to `Application > Restore`
- Select the `BottleFiller.apa` file from the `InTouchProject/` directory

### 2. Configure Tags
- Launch **WindowMaker**
- Load the `Tagname.x` tag file
- Configure I/O addresses or use internal memory tags
- Make sure all digital/analog inputs and outputs are properly mapped

### 3. Run the HMI
- Open **WindowViewer**
- Monitor the filling process on screen
- Use control buttons to Start/Stop and trigger emergency functions
- Observe bottle count, alarm messages, and tank levels

### 4. Hardware Interface (Optional)
- Connect PLC with sensors and actuators
- Use OPC/DA or direct communication protocol in tag configuration
- Ensure real-time data exchange between SCADA and hardware

## Future Enhancements
- Add data logging and report generation using Wonderware Historian
- Integrate trend graphs for performance monitoring
- Add barcode scanning for batch management
- Enable remote monitoring via cloud dashboard
- Expand to multi-line bottle filling with PLC ladder logic
