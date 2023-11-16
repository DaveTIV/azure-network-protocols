<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols 
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create a resource group and two VM's
- Remote into VM1 
- Use various Network Protocols(Ping,ICMP,SSH,TCP/RDP)


<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/X7Wz3tq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I have created two Virtual Machines within a Resource group"RG-LAB-02". VM1 has a windows 10 and VM2 has a Linux(Ubuntu) server.
</p>
<img src="https://i.imgur.com/HcrHV1f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
To remote into VM1, I opened the "Remote Desktop" app and used VM1's IP Address, then logged in with user credentials.
</p>
<img src="https://i.imgur.com/96d2DfQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Inside of VM1, I went to google.com, then to Wireshark and downloaded the Windows x64 version
<img src="https://i.imgur.com/Z1EyZxH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Inside of VM1 I typed ICMP for traffic flow and then I opened Command Prompt and made a ping to VM2 by using VM2 private IP Address.
</p>
<img src="https://i.imgur.com/2D5C9bA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> 
Here I went into VM2's Network Security Group>Inbound Security Rules to add a rule for testing. I created the rule to deny any ICMP traffic.
</p>
<img src="https://i.imgur.com/JLOutnp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
At the ethernet I used SSH, and in the Command line I created a successful SSH tunnel into VM2.
<img src="https://i.imgur.com/wDbxV31.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I am using a TCP port22 connection with traffic.
<img src="https://i.imgur.com/hHE9gS7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I used DHCP with the command line "ipconfig /renew"
<img src="https://i.imgur.com/K4VZ1zz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I used DNS with the command line "nslookup".
<img src="https://i.imgur.com/FtbRaDK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I used UDP Port53 and the command line "nslookup" for Disney.com
<img src="https://i.imgur.com/9M673os.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I used TCP Port 3389 which is also RDP.

