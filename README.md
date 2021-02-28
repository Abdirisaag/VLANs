# VLANsVLANs
=========


Configure PCs with IP address Verify reachability 
==================================================
From PC1 ping 192.168.10.2


ON Switch CLI Create VLANs
==========================
en
conf t
vlan 10
name Accountant
vlan 20
name Marketing
vlan 30
name Sales
exit

Verify VLANs
===========
show vlan brief


Assign Access ports for each VLANs
==================================
conf t
int range fa0/1-4
switchport mode access
switchport access vlan 10
int range fa0/5-6
switchport mode access
switchport access vlan 20
int range fa0/7-8
switchport mode access
switchport access vlan 30
int range fa0/9-10
switchport mode access
switchport access vlan 20
int range fa0/11-12
switchport mode access
switchport access vlan 10
end
copy running-config startup-config 

Verify VLANs Ports
========================

show vlan brief


On PC1 veryify the reachability to Other PC same VLANs or different VLANs
========================================================
ping 192.168.10.6 (reachable)

ping 192.168.20.1 (Unreachable)

ping 192.168.30.1 (Unreachable)
copy running-config startup-config 
