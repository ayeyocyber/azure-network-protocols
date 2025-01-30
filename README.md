<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, I observed various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2> Description </h2>
<p>
In this lab I created 2 vm's in azure one linux ubuntu vm and the other was windows 10.I was trying to ping the linux servers ip from the windows vm and inspect its network traffic in WireShark.
</p>
<br />

<h2>Observations from my labs</h2>

<p>
<img width="1680" alt="Screenshot 2025-01-20 at 10 30 58 PM" src="https://github.com/user-attachments/assets/27ff7701-3f5f-45ed-8860-cc1aebef5805" />
</p>
<p>
a series of ping tests are being run between two devices, with each ping request being followed by a reply. The raw packet data also shows additional information about the ping content.
</p>
<br />

<p>
<img width="1680" alt="Screenshot 2025-01-20 at 10 39 09 PM" src="https://github.com/user-attachments/assets/0183368b-01af-4102-8659-f1fbdeeb2f33" />
</p>
<p>
this highlights the SSH connection establishment process, with encrypted communication and key exchange operations visible in the packet data. It provides a glimpse into the early stages of an SSH connection being secured between two devices.
</p>
<br />

<p>
<img width="1675" alt="Screenshot 2025-01-20 at 10 42 00 PM" src="https://github.com/user-attachments/assets/8d932f9f-0b8d-431a-8fbd-9fe3cdba52ba" />
</p>
<p>
the screenshot shows the DHCP process where the client 10.0.0.4 requests and receives an IP address from the server (168.63.129.16). At the same time, I had PowerShell open showing an unsuccessful SSH login attempt to 10.0.0.5, followed by me renewing the IP address
</p>
<br />

<p>
<img width="1680" alt="Screenshot 2025-01-20 at 10 54 24 PM" src="https://github.com/user-attachments/assets/bc64c878-52d3-4d05-a42e-713b6ff0577a" />
</p>
<p>
 I used nslookup to check if I can resolve the domain Disney.com. It worked, and I got the IP address 130.211.198.204 from the DNS server.
</p>
<br />

<p>
<img width="1677" alt="Screenshot 2025-01-20 at 10 55 52 PM" src="https://github.com/user-attachments/assets/0a9284f9-b627-4b60-ab07-4b0e42ce6f7d" />
</p>
<p>
When i Terminated the connection to the RDP I inspected what happens when the connection terminates.
</p>
<br />
