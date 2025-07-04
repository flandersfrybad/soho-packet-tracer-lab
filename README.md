# soho-packet-tracer-lab

🔍 Preview

[![Watch on TikTok](https://img.shields.io/badge/TikTok-Demo-black?logo=tiktok&logoColor=white&style=for-the-badge)](https://www.tiktok.com/@herrotarrow/video/7522971356372290847)

# 🤝 Let's Connect

[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github&logoColor=white&style=for-the-badge)](https://github.com/flandersfrybad)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white&style=for-the-badge)](https://www.linkedin.com/in/lannertfayad)
[![TikTok](https://img.shields.io/badge/TikTok-Video-black?logo=tiktok&logoColor=white&style=for-the-badge)](https://www.tiktok.com/@herrotarrow/video/7522971356372290847)

🏡 Simple SOHO Network – Cisco Packet Tracer

    A beginner Packet Tracer lab demonstrating a Small Office/Home Office (SOHO) network topology with static IPs and basic connectivity using ping.

🧠 Goal

Establish a working connection between a personal computer (PC0) and a server (Server0) through a single router (Router0), using only static IP addressing and command-line configuration.
🖥️ Topology

[PC0] ←→ [Router0] ←→ [Server0]

PC0 IP:      192.168.0.10/24  
Router0 Inside (Fa0/0): 192.168.0.1/24  
Router0 Outside (Fa0/1): 10.0.0.1/24  
Server0 IP:  10.0.0.2/24

No default gateways, NAT, DNS, or ACLs. This lab is Layer 3 only: basic reachability.
⚙️ Configuration Steps (CLI)

Router0

enable
configure terminal

interface FastEthernet0/0
 ip address 192.168.0.1 255.255.255.0
 no shutdown

interface FastEthernet0/1
 ip address 10.0.0.1 255.255.255.0
 no shutdown

PC0

IP Address:     192.168.0.10  
Subnet Mask:    255.255.255.0  
Default Gateway: (leave blank)

Server0

IP Address:     10.0.0.2  
Subnet Mask:    255.255.255.0  
Default Gateway: (leave blank)

✅ Test

From PC0:

ping 192.168.0.1  ✅
ping 10.0.0.2     ❌ (Fails - different network, no route)

🔍 Learning Outcome

    Understand how routers connect two networks

    Recognize the role of a default gateway in cross-subnet communication

    Use ping and interface configuration to verify Layer 3 connectivity

    Practice Cisco CLI basics

💡 Next Steps

    Add default gateway and enable full ping path

    Add NAT and simulate internet access

    Add ACLs to filter traffic

    Simulate DNS and web traffic
