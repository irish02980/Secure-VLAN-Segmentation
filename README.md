# Secure-VLAN-Segmentation
Cisco Packet Tracer Lab: Implementing Router-on-a-Stick with Management Plane Hardening (ACLs)
Author: Iris Hernandez
Technology: Cisco Packet Tracer, 802.1Q Trunking, Standard ACLS

PROJECT OVERVIEW
This project aims to demonstrate the implementation of a route-on-a-stick, designed to secure a network's management infrastructure. By creating a dedicated Management VLAN (VLAN 99) and applying a Standard Access Control List (ACL) at the gateway, I successfully isolated critical infrastructure management from the general user segment (VLAN 1), preventing unauthorized access while maintaining administrative reachability.

ISSUES AND TROUBLESHOOTING
PHYSICAL INTERFACE ACTIVATION & "PARENT-CHILD" HIERARCHY
While configuring the router-on-a-Stick, the logical sub-interfaces (G0/0.1 & G0/0.99) remained in a down state despite having correct IP addresses.
THE DIAGNOSES: I executed the show ip interface brief command to audit the status of all the ports. Here is where I noticed that GigabitEthernet0/0 was administratively down, meaning the physical port was locked; therefore, the subinterfaces under the port were also down.
THE SOLUTION: I then went to the G0/0 configuration mode and implemented the no shutdown command, which opened the interface and all subinterfaces. To ensure changes were properly saved, a second status check was run, and user gateways were fully operational.  
![Interface Status](interface.png)

LAYER 2 ENCAPSULATION REQUIREMENT (802.1Q)
