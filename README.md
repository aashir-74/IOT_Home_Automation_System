# Smart Home IoT Automation System

A secure, event-driven smart home environment designed and implemented in Cisco Packet Tracer. The system combines network infrastructure, IoT devices, sensor-driven automation, remote monitoring, and programmable control to create a responsive and connected home ecosystem.

By integrating security monitoring, environmental sensing, and automated device control, the platform demonstrates how modern IoT technologies can work together to improve convenience, visibility, and operational efficiency while maintaining secure network boundaries.

![Smart Home Network Topology](assets/Smart_Home_Network_Topology.png)

---

## Overview

The solution is built around a segmented architecture consisting of a private home network and an external internet-facing network.

The home environment includes:

- Motion detection
- Door monitoring
- Smart lighting
- Webcam surveillance
- Alarm notification
- Temperature monitoring
- Automated irrigation control

These devices communicate through a centralized Home Gateway, enabling coordinated automation while maintaining controlled access to external services.

---

## Intelligent Automation

The system continuously monitors sensor activity and automatically responds to events without requiring user intervention.

### Security Response

When motion is detected or a door is opened, the system automatically:

- Turns on the lamp
- Activates the webcam
- Triggers the alarm siren

When no activity is detected:

- The lamp is switched off
- The webcam is disabled

### Environmental Response

When the temperature rises above **25°C**:

- The lawn sprinkler is activated automatically

These rules enable the environment to react dynamically to both security and environmental conditions.

![Automation Rules](assets/IOT_Automation_Rules.png)

---

## Programmable Device Control

Automation within the smart home is extended through Python-based logic running on a Single Board Computer (SBC).

The SBC reads device states and executes control actions, providing an additional layer of programmable intelligence beyond standard IoT automation rules. This approach enables custom behaviour and demonstrates how software-driven decision making can be integrated directly into connected environments.

![Python Automation](assets/SBC_Python_Automation.png)

---

## Network Architecture

The implementation incorporates several core networking components:

- IPv4 addressing and routing
- Wireless network connectivity
- DNS services
- Device registration services
- Home Gateway management
- Network Address Translation (NAT)
- Internal and external network segmentation

The architecture allows internal devices to communicate with external services while preventing unsolicited inbound access from the internet, reflecting a common security model used in real-world smart home deployments.

---

## Validation and Testing

The environment was validated through multiple connectivity and communication tests to verify correct routing, addressing, service availability, and end-to-end connectivity.

| Source | Destination | Result |
|----------|-------------|----------|
| Laptop | Registrar Server | Successful |
| Smartphone | Wireless Router | Successful |
| Laptop | Cloud DNS Server | Successful |
| PC1 | PC2 | Successful |
| Registrar Server | Laptop | Blocked by NAT (Expected Behaviour) |

![Connectivity Testing](assets/Connectivity_Testing.png)

The successful test results confirm reliable communication between network segments, IoT devices, infrastructure services, and remote endpoints while preserving the intended security boundaries.

---

## Technologies

- Cisco Packet Tracer
- Internet of Things (IoT)
- Python
- IPv4 Networking
- DNS
- NAT
- Wireless Networking
- Network Segmentation
- Event-Driven Automation
