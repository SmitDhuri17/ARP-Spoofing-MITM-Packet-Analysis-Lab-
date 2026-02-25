Defensive Strategies Against ARP Poisoning
While this lab demonstrates how an ARP attack is executed, real-world network security relies on multiple layers of defense to prevent and detect such activities.

1. Static ARP Entries
The most direct way to prevent spoofing on critical devices is to manually bind a MAC address to an IP address. This ensures the computer ignores any unsolicited ARP replies sent by an attacker.

Windows Command: arp -s <IP_Address> <MAC_Address>

Linux Command: ip neigh add <IP_Address> lladdr <MAC_Address> dev <interface> nud permanent

2. Dynamic ARP Inspection (DAI)
On professional enterprise networks, hardware-level security is used. Dynamic ARP Inspection (DAI) is a security feature on network switches that intercepts, logs, and discards ARP packets with invalid IP-to-MAC address bindings.

3. VPN (Virtual Private Network) Usage
Using a VPN provides a layer of encryption over all network traffic. Even if an attacker successfully executes an ARP spoofing attack and captures the packets in Wireshark, they will only see encrypted gibberish instead of the raw data.

4. Network Monitoring & Detection Tools
Active monitoring can alert administrators to an attack in progress.

arpwatch: A tool that monitors ethernet activity and maintains a database of ethernet/IP address pairings, sending alerts when a pairing changes unexpectedly.

XArp: An advanced detection tool that uses different inspection modules to discover ARP spoofing attempts.
