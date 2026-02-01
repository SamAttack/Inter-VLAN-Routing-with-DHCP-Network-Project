📡 Inter-VLAN Routing with DHCP (Cisco Packet Tracer)


📘 Project Overview

This project demonstrates the implementation of VLAN segmentation, inter-VLAN routing (router-on-a-stick), and dynamic IP address allocation using DHCP in Cisco Packet Tracer.

Two departments (HR and SALES) are separated into different VLANs.
A single router interface is configured with subinterfaces to route between VLANs, and the router is also configured as a DHCP server to automatically assign IP addresses to hosts in each VLAN.

This project simulates a small business network using enterprise networking principles.



🧩 Network Topology

Devices Used:

1 × Cisco Router (1941)

1 × Cisco Switch (2960)

4 × PCs

VLAN Design:

VLAN	Name	Network	Gateway
10	HR	192.168.10.0/24	192.168.10.1
20	SALES	192.168.20.0/24	192.168.20.1
🖥️ IP Addressing (via DHCP)

All PCs receive IP addresses dynamically from the router.

HR VLAN (10)

Network: 192.168.10.0/24

Gateway: 192.168.10.1

SALES VLAN (20)

Network: 192.168.20.0/24

Gateway: 192.168.20.1



⚙️ Configuration Summary
Switch Configuration

Created VLAN 10 (HR) and VLAN 20 (SALES)

Assigned access ports:

Fa0/1–Fa0/2 → VLAN 10

Fa0/3–Fa0/4 → VLAN 20

Configured trunk port to router on G0/1

Router Configuration

Configured router-on-a-stick using subinterfaces:

G0/0.10 → VLAN 10

G0/0.20 → VLAN 20

Enabled 802.1Q encapsulation

Assigned default gateway IPs

Configured DHCP pools for each VLAN



✅ Verification & Testing

Key verification commands:

show vlan brief
show interfaces trunk
show ip interface brief
show ip dhcp binding
ping


Connectivity tests performed:

HR → HR communication ✔

SALES → SALES communication ✔

HR → SALES communication ✔

SALES → HR communication ✔

PCs receive IP addresses automatically via DHCP ✔

🧠 Skills Demonstrated

VLAN configuration

802.1Q trunking

Router-on-a-stick inter-VLAN routing

DHCP server configuration

IP addressing and subnetting

Network verification and troubleshooting

Cisco IOS CLI usage

📂 Files Included

.pkt topology file

README.md

PDF configuration guide

Screenshots of:

VLAN configuration

Trunk configuration

DHCP bindings

Successful ping tests

🚀 Future Improvements

Implement ACLs to restrict inter-VLAN access

Add multiple switches with trunk links

Add NAT and internet access

Implement port security

Migrate routing to a Layer 3 switch

🏁 Conclusion

This project demonstrates a realistic enterprise networking scenario using VLAN segmentation, inter-VLAN routing, and centralized DHCP services.
It reflects core concepts required for CCNA and CompTIA Network+ and showcases practical network configuration skills.