**AWS Data Center Network Architecture**

Secure, Scalable & Highly Available Enterprise Network Design 

**📌 Project Overview**

This project simulates a large-scale, enterprise-grade AWS-inspired data center network designed using a hierarchical architecture (Core, Distribution, and Access layers). The topology was engineered to reflect real-world network design principles used in modern enterprise and cloud infrastructure environments.

The network integrates multi-area OSPF, VLAN segmentation at scale (14 VLANs across departments), Layer 3 switching, first-hop redundancy, secure routing authentication, and link aggregation to ensure high availability, scalability, and fault tolerance.

Rather than a simple connectivity lab, this project focuses on architectural depth, control-plane stability, and resilient network design under complex operational conditions.


🧠 **Objectives**

✅ Design a scalable enterprise campus and data center network

✅ Implement redundancy at Layer 2 and Layer 3

✅ Deploy secure dynamic routing using OSPF with authentication

✅ Provide inter-VLAN routing using multilayer switches

✅ Ensure high availability using HSRP and EtherChannel

✅ Enable full connectivity between all departments and services

✅ Simulate real-world enterprise networking challenges


🏗️ **Network Architecture Design**

**🔹 Hierarchical Model Implemented**

Core Layer: Central backbone router (R4) acting as OSPF backbone (Area 0)

🧩Distribution Layer: Multiple Layer 3 switches with SVIs, HSRP, and inter-VLAN routing

🧩Access Layer: Departmental switches connected to end devices

Edge Connectivity: Cloud-facing links with IP routing enabled for external reachability

This structure mirrors real enterprise and data center network deployments.


**🌐 Routing & Control Plane Engineering**

📍Multi-Area OSPF Design

📍Area 0 (Backbone) – Core Router (R4)

📍Area 1 – Right Enterprise Segment

📍Area 2 – Left Enterprise Segment

Area 3 – Lower Infrastructure Segment

OSPF + Static Route Redistribution for flexible route propagation

All VLAN networks advertised into OSPF for full Layer 3 reachability

Loopbacks configured on routers and L3 switches for stable router IDs

MD5 authentication enabled on OSPF adjacencies for routing security

This design enhances scalability, network isolation, reduces LSA flooding, and improves convergence speed in large topologies. 


🧩 **VLAN & Segmentation Strategy**

14 VLANs deployed representing 14 departments/offices

Department-based logical segmentation

SVIs configured only for locally hosted VLANs per Distribution Switch

Full inter-VLAN routing via Layer 3 switches

Trunk links between Access and Distribution layers

VLAN networks dynamically integrated into OSPF domain

The network supports 14 enterprise departments mapped into multiple VLAN ranges including:

- Infrastructure Engineering

- Cybersecurity

- Reception

- Data Center Operations

- Conference & Automation

- AWS DevOps

- Storage & Backup Systems

- Dining & Facilities

- IoT / Workload Systems

- Global NOC

This approach reflects enterprise-grade segmentation and traffic isolation.

**⚡ High Availability & Redundancy Mechanisms**

**HSRP (First Hop Redundancy)**

✔ Active/Standby HSRP configured per VLAN

✔ Gateway redundancy across paired Distribution L3 switches

✔ Seamless failover for end-user network continuity

**EtherChannel (LACP)**

🔹LACP (Active/Active) used for aggregated uplinks

🔹Redundant links between Access and Distribution layers

Increased bandwidth + link-level fault tolerance

**Spanning Tree Optimization***

Rapid-PVST deployed across L2 and L3 switches

🟢Loop prevention in a multi-path redundant topology

Optimized convergence for enterprise switching environments

🔐 **Security Implementation**

MD5 authentication on OSPF routing adjacencies

🟢Secure control-plane communication between routers and L3 switches

🟢Segmented VLAN architecture reducing lateral attack surface

Structured routing domain with authenticated neighbors

☁️ **Infrastructure & Cloud Connectivity**

📌Routed links between Distribution Layer and Routers (Layer 3 links)

📌IP routing enabled on all Layer 3 switches

External cloud-facing connectivity simulated

Static route redistribution to maintain hybrid routing logic

DHCP relay (IP Helper) implemented for centralized address management (select segments)

**Challenges & Engineering Experience**

This project required extensive troubleshooting and iterative design refinement, particularly in:

🔷Multi-area OSPF adjacency formation

🔷Layer-2 loop prevention with redundant paths

🔷Route propagation across segmented OSPF areas

🔷Control-plane authentication and adjacency validation

HSRP synchronization across distribution switches

VLAN propagation and trunk consistency

Authentication mismatches in routing domains

Route advertisement across hierarchical boundaries

The complexity of the environment strengthened my practical skills in network diagnostics, protocol behavior analysis, enterprise-scale configuration management and systematic problem solving — essential competencies for production network environments.

**Key Outcomes**

✔ Full end-to-end connectivity across all departments

✔ Scalable and modular network architecture

✔ Secure and authenticated routing domain

✔ Fault-tolerant gateway redundancy

✔ Optimized bandwidth via link aggregation

✔ Enterprise-grade segmentation and routing design

Author = **Bradley Giovanni**

Aspiring Network Engineer | CCNA Candidate | NOC ENGINEER | Network Administrator

Focused on Enterprise Networking, NOC Operations, and Infrastructure Design

 [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/bradley-giovanniii293)
