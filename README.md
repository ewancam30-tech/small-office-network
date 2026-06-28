# Small Office Network Deployment

## Project Overview

This project demonstrates the design, deployment, configuration, and verification of a secure small office network using Cisco Packet Tracer.

The objective was to build a reliable network infrastructure capable of supporting multiple employees while implementing industry best practices for IP addressing, device configuration, DHCP services, secure management, and network verification.

---

## Business Scenario

Campbell Technologies has expanded from a single workstation to a 20-person office consisting of three departments:

* Administration
* Sales
* IT

The company requires a secure and scalable network to support employee communication, printer access, and future growth. As the Network Engineer, I was responsible for designing, implementing, testing, and documenting the network deployment.

---

## Project Objectives

* Design a small office network
* Configure Cisco router and switch
* Implement IPv4 addressing
* Configure DHCP services
* Configure switch management
* Configure secure administrative access using SSH
* Verify network connectivity
* Troubleshoot configuration issues
* Document the complete deployment process

---

## Network Topology

<img width="373" height="256" alt="image" src="https://github.com/user-attachments/assets/41aac91e-3d78-4be2-8c7b-8a3cf3be84fc" />




---

## Equipment

| Device                | Quantity |
| --------------------- | -------: |
| Cisco Router          |        1 |
| Cisco Catalyst Switch |        1 |
| PCs                   |        3 |
| Network Printer       |        1 |

---

## IP Addressing Plan

| Device  | Interface | IP Address    |
| ------- | --------- | ------------- |
| R1      | G0/0      | 192.168.10.1  |
| SW1     | VLAN 1    | 192.168.10.2  |
| Printer | NIC       | 192.168.10.50 |
| PC1     | DHCP      | Automatic     |
| PC2     | DHCP      | Automatic     |
| PC3     | DHCP      | Automatic     |

Subnet Mask

255.255.255.0

Default Gateway

192.168.10.1

DNS Server

8.8.8.8

---

## Technologies Used

* Cisco Packet Tracer
* Cisco IOS
* IPv4
* DHCP
* SSH
* Cisco CLI

---

## Skills Demonstrated

* Network design
* Router configuration
* Switch configuration
* DHCP implementation
* IPv4 addressing
* Secure device management
* Network verification
* Technical documentation
* Troubleshooting

---

## Configuration Tasks Completed

* Configured router hostname
* Configured switch hostname
* Assigned IPv4 addresses
* Configured switch management interface
* Configured DHCP pools
* Configured default gateway
* Configured SSH remote management
* Configured console security
* Saved device configurations
* Verified connectivity between all devices

---

## Verification

The following commands were used to validate the deployment:

```text
show ip interface brief

show running-config
show ip dhcp binding
show ip dhcp pool
show version
ping
tracert
```

---

## Screenshots

### Network Topology

![Topology](screenshots/01_topology.png)

---

### Router Configuration

<img width="192" height="451" alt="image" src="https://github.com/user-attachments/assets/d8d908ea-8324-48e1-a19d-a2bd6a22afab" />
<img width="107" height="198" alt="image" src="https://github.com/user-attachments/assets/e7a4d246-8b7e-4ac8-ab8d-07caa70667e8" />



---

### Switch Configuration

<img width="135" height="443" alt="image" src="https://github.com/user-attachments/assets/df01fda7-48b8-4a4d-aead-387daea09aad" />
<img width="116" height="364" alt="image" src="https://github.com/user-attachments/assets/5ba725e3-ac74-46a8-9b0e-cf65256141f3" />


---

### DHCP Configuration

<img width="189" height="128" alt="image" src="https://github.com/user-attachments/assets/185a9e6f-48ac-4e6e-bcab-849229fbcc89" />
<img width="200" height="126" alt="image" src="https://github.com/user-attachments/assets/f39c94e0-d740-4db8-b905-007a96caa99a" />
<img width="209" height="132" alt="image" src="https://github.com/user-attachments/assets/d1af8c78-eaa3-4b19-9bf2-88910409e25a" />

### Printer Configuration

<img width="356" height="179" alt="image" src="https://github.com/user-attachments/assets/0c8bb986-a424-48e8-954b-5a246a3ffd1e" />
<img width="351" height="165" alt="image" src="https://github.com/user-attachments/assets/be61731a-f6c7-4c00-b18d-7ed135e7ee02" />

---

### Successful Connectivity Test

<img width="211" height="94" alt="image" src="https://github.com/user-attachments/assets/84cd74c1-fa5d-4c5f-9d52-0273bc9bde88" />
<img width="212" height="93" alt="image" src="https://github.com/user-attachments/assets/d8c7f385-2d2c-4242-9d61-38c148674553" />
<img width="208" height="94" alt="image" src="https://github.com/user-attachments/assets/dbe102e9-5e46-4364-82c3-7ddff3298c13" />

<img width="293" height="157" alt="image" src="https://github.com/user-attachments/assets/42af34e5-f13c-4ba1-84a4-741283c9d5c8" />
<img width="304" height="137" alt="image" src="https://github.com/user-attachments/assets/6e688d3b-0df1-47ee-97ea-8355a5334fe6" />

---

## Troubleshooting

### Issue

A workstation did not receive an IP address from the DHCP server.

**Cause**

The DHCP pool network statement was configured incorrectly.

**Resolution**

Corrected the DHCP network configuration and renewed the client lease.

---

### Issue

Unable to ping the default gateway.

**Cause**

The router interface was administratively down.

**Resolution**

Enabled the interface using the `no shutdown` command.

---

### Issue

The switch could not be managed remotely.

**Cause**

The management VLAN interface did not have an IP address assigned.

**Resolution**

Configured the VLAN 1 management interface with an IPv4 address and default gateway.

---

## Lessons Learned

This project reinforced the importance of careful network planning, structured device configuration, and systematic verification during deployment.

Key takeaways include:

* Proper IP addressing simplifies network management.
* DHCP reduces manual configuration errors.
* Verification after every configuration change helps identify issues early.
* Secure remote management using SSH is preferable to unsecured protocols.
* Thorough documentation improves maintainability and troubleshooting.

---

## Future Improvements

Future enhancements to this network include:

* VLAN segmentation
* Inter-VLAN routing
* Access Control Lists (ACLs)
* Port Security
* OSPF routing
* Redundant network links
* Wireless access integration
* Network monitoring and logging

---

## Project Roadmap

* ✅ Project 1: Cisco Device Basics
* ✅ Project 2: Small Office Network Deployment
* ⬜ Project 3: VLAN Segmentation
* ⬜ Project 4: Inter-VLAN Routing
* ⬜ Project 5: Static Routing
* ⬜ Project 6: RIP Routing
* ⬜ Project 7: EIGRP Enterprise Network
* ⬜ Project 8: OSPF Enterprise Network
* ⬜ Project 9: Network Security
* ⬜ Project 10: Enterprise Network Acquisition (RIP ↔ EIGRP)
* ⬜ Project 11: Campus Network
* ⬜ Project 12: Enterprise Network Capstone

---

## Author

**Ewan Campbell**

CompTIA A+ Certified

CompTIA Network+ Certified

Associate of Science in Network Systems Technology (Cybersecurity)

Aspiring Cybersecurity and Network Professional
