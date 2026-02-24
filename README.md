# ARP-Spoofing-MITM-Packet-Analysis-Lab-

A "Swiss Army knife" lab for ARP Poisoning and MITM attacks in an isolated VMware environment. This project uses Bettercap for reconnaissance and active spoofing, with Wireshark for deep packet analysis. Validated with "before and after" ARP evidence to prove successful traffic interception.

Executive Summary:

This project documents the simulation of a Man-in-the-Middle (MITM) attack using ARP Cache Poisoning. The lab demonstrates how a security professional can exploit vulnerabilities in the Address Resolution Protocol (ARP) to intercept and analyze network traffic in real-time. By using Bettercap as a multi-functional exploitation framework, the lab covers the entire attack lifecycle from reconnaissance to post-exploitation analysis.

Technical Objectives:

Infrastructure Setup: Designing a secure, isolated NAT network using VMware Workstation to host an attacker (Kali Linux) and a victim (Windows 10).
Protocol Baseline: Establishing a "clean" network state by documenting the victim’s legitimate ARP table and gateway connection.
Network Reconnaissance: Utilizing Bettercap’s net.probe and net.show modules to map the local subnet and identify targets.
Active Spoofing: Executing arp.spoof to redirect the victim's traffic through the attacker's machine.
Packet Interception: Using Wireshark and net.sniff to capture and inspect live data packets traveling between the victim and the gateway.

Lab Specifications:

Attacker Node: Kali Linux 2024.x (4GB RAM / 4 Processors).
Victim Node: Windows 10 (4GB RAM / 2 Processors).
Environment: Isolated VMnet8 (NAT) network (Subnet: 192.168.222.0/24).

Key Outcomes

Proof of Concept: Successfully changed the victim's gateway MAC address from its legitimate state to the attacker’s MAC address.
Data Visibility: Demonstrated that unencrypted traffic (HTTP/DNS) can be clearly read and analyzed once the MITM position is established.
