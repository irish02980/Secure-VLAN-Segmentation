# Secure-VLAN-Segmentation
Cisco Packet Tracer Lab: Implementing Router-on-a-Stick with Management Plane Hardening (ACLs)
Author: Iris Hernandez
Technology: Cisco Packet Tracer, 802.1Q Trunking, Standard ACLS

PROJECT OVERVIEW
This project aims to demonstrate the implementation of a route-on-a-stick, designed to secure a network's management infrastructure. By creating a dedicated Management VLAN (VLAN 99) and applying a Standard Access Control List (ACL) at the gateway, I successfully isolated critical infrastructure management from the general user segment (VLAN 1), preventing unauthorized access while maintaining administrative reachability.

ISSUES AND TROUBLESHOOTING
1. As I was configuring the router to be a Router-on-a-Stick, I tried to assign an IP address to the sub-interfaces, but they showed as "Administratively Down." In order to troubleshoot, I had to look at the interface and ran the following 
command: show ip interface brief. 
![Interface Status](interface.png)
