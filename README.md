# Cybersecurity Homelab
A virtual security environment built to simulate enterprise infrastructure and security monitoring. This homelab was used to practice troubleshooting, monitoring, and security skills in a controlled environment. 

# Setup
All machines were setup using VMware, a platform for running multiple virtual machiens from a single host. In this lab, I created and configured the following:
- pfSense: This was used as the firewall and router for the machines.
- Windows Server 2019: Served as an active director and domain controller, managing the windows 10 client (user).
- Windows 10 client: The endpoint device.
- Splunk: SIEM to conduct log analysis.
- Security Onion: An Intrusion Detection System (IDS) used for intrusion detection and monitoring.
- Kali Linux: The attack machine to practice attacking and defense for the machines.

# Scenarios/Demonstrations
1. Attack and Detection Simulation:
   - Goal: Demonstrate a safe and contained enumeration activity from an attacker (Kali Linux) and show detection and loggin in Splunk.
   - Summary:
       1. Scanned the lab subnet to find the domain controller.
       2. Veriefied open SMB ports on the domain controller.
       3. Authenticated to SMB as a domain user.
       4. Confirmed the resulting Windows Security events (4624) were shipped to Splunk. 
   
