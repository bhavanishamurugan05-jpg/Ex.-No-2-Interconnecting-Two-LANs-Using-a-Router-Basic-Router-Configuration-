# Date :27/10/26
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>

<img width="1811" height="826" alt="Screenshot 2026-10-27 181057" src="https://github.com/user-attachments/assets/9eb1b644-f95a-429c-a0ca-2eeca6706b41" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>

<img width="1588" height="825" alt="Screenshot 2026-10-27 182340" src="https://github.com/user-attachments/assets/911ab2c9-cfdb-4451-9c8a-c5821c8b42b5" />

•	IP configurations on PCs<br>

<img width="1370" height="670" alt="Screenshot 2026-10-27 182402" src="https://github.com/user-attachments/assets/cda8eb9a-9704-45ec-a0f8-fd28abd64aad" />

<img width="1348" height="711" alt="Screenshot 2026-10-27 182412" src="https://github.com/user-attachments/assets/8d24c085-2fe0-4cc5-8aef-6a331c7ccb44" />

•	Successful ping between PC0 and PC1<br>
<img width="1572" height="922" alt="Screenshot 2026-10-27 182209" src="https://github.com/user-attachments/assets/190d4248-ea3d-4455-9674-d29a66ec55cd" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

