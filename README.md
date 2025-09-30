Include these sections:

Title

Task 4: Setup and Use Windows Firewall


Objective

Configure and test basic firewall rules on Windows to allow or block traffic.

Understand how firewall filters network traffic.

Tools Used

Windows Firewall (Built-in)

Steps Performed

Opened Windows Firewall (Win + R → wf.msc)

Listed current firewall rules:

netsh advfirewall firewall show rule name=all


Blocked inbound Telnet (port 23):

netsh advfirewall firewall add rule name="Block Telnet" protocol=TCP dir=in localport=23 action=block


Verified the rule:

netsh advfirewall firewall show rule name="Block Telnet"


Tested the rule:

Open Command Prompt and try: telnet 127.0.0.1 23

Connection should fail.

Removed test block rule:

netsh advfirewall firewall delete rule name="Block Telnet"


Screenshots / Evidence

Screenshot of Windows Firewall showing the rule added.

Screenshot of netsh output showing the rule applied.

Summary

Windows Firewall filters traffic based on rules (ports, IPs, protocols).

Inbound rules control incoming traffic.

Blocking Telnet improves security because it’s insecure and transmits data in plain text.

Interview Prep (Optional)

What is a firewall?

Difference between stateful/stateless firewall

Inbound and outbound rules

Why block port 23 (Telnet)

How firewall improves network security
