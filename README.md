# 🌐 Computer Networks Lab Portfolio

### Practical Networking Experiments | Cisco Packet Tracer | Network Configuration & Design

## 📌 About This Repository

Welcome to my **Computer Networks Lab Repository**, a structured collection of practical experiments, configuration exercises, network simulations, and design tasks completed as part of my Computer Networks coursework in the Department of Software Engineering at the University of Azad Jammu and Kashmir, Muzaffarabad.

This repository documents my hands-on learning journey in computer networking, beginning with Cisco Packet Tracer installation and basic LAN communication, and progressing toward router configuration, switch operation, MAC address learning, VLAN implementation, and inter-VLAN routing.

The purpose of this repository is to connect theoretical networking concepts with practical implementation. Through these experiments, I explore how devices communicate, how switches forward network traffic, how routers connect different networks, and how network configurations can be designed for organizational environments.

> **From basic connectivity to structured network design — this repository documents my practical exploration of Computer Networks.**

## 🎯 Repository Objectives

The main objectives of this repository are:

* Develop practical understanding of fundamental computer networking concepts.
* Learn to create and simulate network topologies using Cisco Packet Tracer.
* Configure and verify network devices using Cisco IOS CLI commands.
* Understand the relationship between physical connectivity and logical network configuration.
* Practice IPv4 addressing and basic LAN communication.
* Explore switching concepts, including MAC address learning.
* Understand VLAN segmentation and trunk communication.
* Implement and analyze inter-VLAN routing using Router-on-a-Stick.
* Design a small organizational network considering connectivity, separation, and future expansion.
* Maintain organized documentation of laboratory experiments and results.

## 🧪 Laboratory Experiments

### 📘 Lab 01 — Cisco Packet Tracer Installation

**Focus:** Network simulation environment setup

This lab covers the installation and initial verification of Cisco Packet Tracer on a Windows 64-bit operating system.

**Key activities:**

* Installation using the setup wizard.
* Understanding installation requirements.
* Launching and verifying the simulation software.
* Preparing the environment for practical networking experiments.

**Concepts explored:** Network simulation, software setup, and laboratory preparation.

### 📘 Lab 02 — Basic LAN Network Topology

**Focus:** Local Area Network connectivity and IPv4 configuration

A simple LAN topology is created using two PCs connected to a switch.

**Key activities:**

* Creating a basic LAN in Cisco Packet Tracer.
* Connecting PCs using copper straight-through cables.
* Assigning static IPv4 addresses.
* Configuring devices within the same subnet.
* Verifying connectivity using `ipconfig` and `ping`.

**Concepts explored:** LAN, IPv4 addressing, subnet masks, switches, and connectivity testing.


### 📘 Lab 03 — Physical Layer of the OSI Model

**Focus:** Ethernet cable termination and physical connectivity

This experiment explores the Physical Layer of the OSI model through Ethernet cable termination using RJ45 connectors.

**Key activities:**

* Working with UTP cable.
* Preparing and arranging Ethernet cable wires.
* Applying the T568B wiring standard.
* Using an RJ45 connector and crimping tool.
* Testing the completed cable using a network cable tester.

**Concepts explored:** OSI Physical Layer, Ethernet cabling, RJ45 connectors, T568B wiring, and physical-layer reliability.

---

### 📘 Lab 04 — Router CLI Access and Configuration

**Focus:** Cisco router command-line interface

This lab introduces router access and basic security configuration using Cisco IOS CLI in Packet Tracer.

**Key activities:**

* Accessing the router CLI.
* Understanding User EXEC, Privileged EXEC, and Global Configuration modes.
* Configuring router passwords.
* Enabling password encryption.
* Viewing running and startup configurations.
* Saving the running configuration to startup configuration.

**Example commands:**

```text
enable
configure terminal
enable password cisco123
service password-encryption
enable secret class123
show running-config
show startup-config
copy running-config startup-config
```

**Concepts explored:** Cisco IOS CLI, configuration modes, device security, RAM, NVRAM, and configuration persistence.

---

### 📘 Lab 05 — Interconnecting Two Switches

**Focus:** LAN expansion and communication across switches

This experiment connects two switches and six PCs to demonstrate communication between devices attached to different switches.

**Key activities:**

* Creating a topology using two switches and six PCs.
* Connecting the switches using Ethernet.
* Assigning IP addresses to the PCs.
* Testing communication using ICMP.
* Observing packet flow in Cisco Packet Tracer Simulation Mode.

**Concepts explored:** Switch interconnection, Ethernet switching, ICMP, simulation mode, and LAN communication.

---

### 📘 Lab 06 — Star Topology Using a Switch

**Focus:** Network topology design and centralized connectivity

This lab demonstrates the implementation of a star topology in which multiple PCs connect to a central switch.

**Key activities:**

* Placing a switch at the center of the topology.
* Connecting multiple PCs using Ethernet cables.
* Assigning IP addresses within the same network.
* Verifying communication using ping.
* Observing packet movement through the switch.

**Concepts explored:** Star topology, centralized switching, network management, and connectivity troubleshooting.

---

### 📘 Lab 07 — Cisco IOS CLI Commands

**Focus:** Network device configuration and verification

This experiment develops familiarity with commonly used Cisco IOS commands for router and switch configuration.

**Key activities:**

* Accessing privileged and configuration modes.
* Selecting interfaces.
* Configuring IPv4 addresses.
* Enabling interfaces using `no shutdown`.
* Verifying interface status.
* Saving device configuration.

**Example commands:**

```text
enable
configure terminal
interface gigabitEthernet 0/0
ip address 192.168.10.1 255.255.255.0
no shutdown
end
show ip interface brief
copy running-config startup-config
```

**Concepts explored:** Cisco IOS CLI, interface configuration, IP addressing, verification, and configuration management.

---

### 📘 Lab 08 — MAC Address Table and Switch Learning

**Focus:** Layer 2 switching and dynamic MAC address learning

This lab investigates how a switch learns and records MAC addresses when network communication takes place.

**Key activities:**

* Creating a small switched network with two PCs.
* Viewing the MAC address table before communication.
* Sending a ping between PCs.
* Observing learned MAC addresses and associated switch ports.
* Clearing dynamic MAC address entries.

**Example commands:**

```text
enable
show mac address-table
clear mac address-table dynamic
show mac address-table
```

**Concepts explored:** MAC addresses, Layer 2 switching, dynamic learning, switch forwarding behavior, and MAC table management.

---

### 📘 Lab 09 — Inter-VLAN Routing Using Router-on-a-Stick

**Focus:** VLAN segmentation and communication between VLANs

This laboratory demonstrates how a router can facilitate communication between separate VLANs using the Router-on-a-Stick method.

The scenario includes two departments:

| Department           | VLAN    | Example Network |
| -------------------- | ------- | --------------- |
| Development (DEV)    | VLAN 10 | 192.168.10.0/24 |
| Human Resources (HR) | VLAN 20 | 192.168.20.0/24 |

**Key activities:**

* Creating VLAN 10 and VLAN 20.
* Assigning switch access ports to the respective VLANs.
* Configuring a switch-to-router trunk.
* Creating router subinterfaces.
* Configuring 802.1Q encapsulation.
* Assigning gateway IP addresses.
* Testing inter-VLAN connectivity using ping.

**Example router configuration:**

```text
enable
configure terminal

interface gigabitEthernet 0/0
no shutdown
exit

interface gigabitEthernet 0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
exit

interface gigabitEthernet 0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0
exit

end
copy running-config startup-config
```

**Verification commands:**

```text
show vlan brief
show interfaces trunk
show ip interface brief
ping <destination-IP>
```

**Concepts explored:** VLANs, access ports, trunking, 802.1Q, router subinterfaces, default gateways, and inter-VLAN communication.


## 🏫 Open-Ended Lab (OEL) — Educational Institute Network Design

### Focus: Network Planning, Topology Selection, Configuration, and Scalability

The open-ended lab extends the practical learning experience into a network design scenario for a newly established educational institute.

The proposed network includes separate departmental areas such as:

* Administration
* Academic / Faculty
* IT / Lab

The implementation is designed as a practical, scaled network model in Cisco Packet Tracer, with departmental switches, connected PCs, router-based communication, and IP subnet planning.

### Main Deliverables

* Network requirements analysis.
* Topology selection and justification.
* Network cabling plan.
* Switch configuration.
* Router configuration.
* IPv4 addressing plan.
* Network diagram.
* Verification and connectivity testing.
* Future expansion recommendations.

### Design Concepts

The OEL explores a hierarchical, star-based network arrangement in which departmental devices connect to access switches and routing is used to facilitate communication between departmental networks.

The report also discusses:

* Cat6 Ethernet cabling.
* Department-specific IPv4 subnets.
* Router-on-a-Stick as a possible routing implementation.
* Configuration templates for network devices.
* Network expansion and scalability considerations.

> The open-ended lab connects individual networking concepts with a practical organizational network design problem.


## 🛠️ Tools and Technologies

| Tool / Technology   | Purpose                                     |
| ------------------- | ------------------------------------------- |
| Cisco Packet Tracer | Network simulation and topology design      |
| Cisco IOS CLI       | Router and switch configuration             |
| IPv4                | Logical addressing and subnet configuration |
| Ethernet            | Wired network connectivity                  |
| ICMP                | Connectivity testing using ping             |
| VLANs               | Logical network segmentation                |
| 802.1Q              | VLAN tagging across trunk links             |
| Router-on-a-Stick   | Inter-VLAN routing                          |
| MAC Address Table   | Layer 2 switch learning analysis            |
| RJ45 / T568B        | Ethernet cable termination                  |


## 📚 Core Networking Concepts Covered

This repository provides practical exposure to the following computer networking concepts:

### Network Fundamentals

* Local Area Networks (LANs)
* Network topologies
* Physical and logical connectivity
* Ethernet cabling
* OSI model — Physical Layer

### IPv4 and Connectivity

* Static IPv4 addressing
* Subnet masks
* Same-subnet communication
* ICMP and ping testing
* Default gateway concepts

### Cisco Device Configuration

* Cisco IOS command modes
* Router CLI access
* Interface configuration
* Password configuration
* Configuration verification
* Running and startup configurations

### Switching

* Switch interconnection
* MAC address learning
* Dynamic MAC address tables
* Access ports
* VLAN creation and assignment
* Trunk interfaces

### Routing

* Router subinterfaces
* 802.1Q encapsulation
* Router-on-a-Stick
* Inter-VLAN communication
* Departmental network segmentation

### Network Design

* Topology selection
* IP addressing plans
* Cabling considerations
* Department-based network organization
* Scalability and future expansion


## 📁 Repository Structure

The laboratory reports are maintained in both editable document and PDF formats.

```text
Computer-Networks/
│
├── README.md
│
├── CN_Lab_01_2024_SE_18.docx
├── CN_Lab_01_2024_SE_18.pdf
│
├── CN_Lab_02_2024_SE_18.docx
├── CN_Lab_02_2024_SE_18.pdf
│
├── CN_Lab_03_2024_SE_18.docx
├── CN_Lab_03_2024_SE_18.pdf
│
├── CN_Lab_04_2024_SE_18.docx
├── CN_Lab_04_2024_SE_18.pdf
│
├── CN_Lab_05_2024_SE_18.docx
├── CN_Lab_05_2024_SE_18.pdf
│
├── CN_Lab_06_2024_SE_18.docx
├── CN_Lab_06_2024_SE_18.pdf
│
├── CN_Lab_07_2024_SE_18.docx
├── CN_Lab_07_2024_SE_18.pdf
│
├── CN_Lab_08_2024_SE_18.docx
├── CN_Lab_08_2024_SE_18.pdf
│
├── CN_Lab_09_2024_SE_18.docx
├── CN_Lab_09_2024_SE_18.pdf
│
├── CN_OEL_2024_SE_18.docx
└── CN_OEL_2024_SE_18.pdf
```

---

## 🔍 Learning Outcomes

After completing these experiments, I developed practical familiarity with:

1. Setting up a network simulation environment.
2. Building and analyzing basic LAN topologies.
3. Understanding physical Ethernet connectivity.
4. Using Cisco IOS CLI for network-device configuration.
5. Assigning and verifying IPv4 addresses.
6. Testing communication between network devices.
7. Understanding how switches learn MAC addresses.
8. Configuring VLANs and trunk links.
9. Implementing Router-on-a-Stick inter-VLAN routing.
10. Planning a small organizational network with departmental separation.


## 🚀 Future Improvements

This repository can be extended with additional networking experiments and supporting materials, including:

* Static routing and dynamic routing protocols.
* DHCP server configuration.
* Access Control Lists (ACLs).
* Network Address Translation (NAT).
* IPv6 addressing and configuration.
* Subnetting and VLSM practice.
* Wireless LAN simulation.
* Network troubleshooting scenarios.
* Improved network diagrams and configuration evidence.
* Additional Packet Tracer project files (`.pkt`).

## 🎓 Academic Context

**Course:** Computer Networks
**Department:** Software Engineering
**Institution:** The University of Azad Jammu and Kashmir, Muzaffarabad
**Repository Type:** Academic Laboratory Portfolio
**Primary Simulation Tool:** Cisco Packet Tracer

## 📄 License

This repository is intended primarily for educational and academic purposes. You may use it as a reference for learning computer networking concepts and Cisco Packet Tracer configurations.
