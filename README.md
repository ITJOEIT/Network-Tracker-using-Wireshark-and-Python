<h1>Network Tracker using Wireshark and Python</h1>

<h2>Description</h2>
For this project, I created a Network Tracker using the packet analyser Wireshark, some Python code and Google Maps. This project demonstrates the implementation steps needed to take a network traffic file and convert it into a visual representation using Google Maps.
<br />

<h2>Environments and Languages Used</h2>

- <b>Wireshark</b>
- <b>Python</b>
- <b>Google Maps</b> 


<h2>Project walk-through:</h2>

<p align="center">
SIEM Diagram: <br/>
<br />
<img src="https://i.ibb.co/tcc9nNr/Image0.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
<br />
First, I captured some network traffic using Wireshark. I created a pcap file. This file consisted of all network traffic going to and from my laptop. To initialise the capture, I selected an interface that the traffic is going through. <br/>
<br />
<img src="https://i.ibb.co/FDpRYNQ/Image1.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
<br />
Create inbound security rules to allow all traffic into the virtual machine:  <br/>
<br />
<img src="https://i.ibb.co/CJ62CXg/Image2.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
<br />
<br />
Create a Log Analytics Workspace. This will be used to ingest logs from the Virtual Machine: <br/>
<br />
<img src="https://i.ibb.co/60pMQf9/Image3.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
<br />
<br />
In Azure Security Environment Settings turn the Azure Defender On and in Data Collection customise it to collect All Events. This will enable the ability to gather logs from virtual machine into the Log Analytics Workspace:  <br/>
<br />
<img src="https://i.ibb.co/PFvvgzt/Image4a.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
<br />
<br />
Run virtual machine and log into it with the IP address using Remote Desktop:  <br/>
<br />
<img src="https://i.ibb.co/2N48C9j/Image5.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
<br />
<br />
In the virtual machine, open Windows Firewall and turn off the firewall in domain, private and public tabs:  <br/>
<br />
<img src="https://i.ibb.co/yB3vQJ6/Image6.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
<br />
<br />
Create a script that uses an API key from an IP Gelocation website:  <br/>
<br />
<img src="https://i.ibb.co/2jyMmHM/Image7.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
<br />
<br />
Create a custom log in Log Analytics Workspace which allows to bring the geo data into the Workspace. Latitude and longitude will be used to identify IP address location:  <br/>
<br />
<img src="https://i.ibb.co/Jcj6N9q/Image8.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/><br />
<br />
Set up a Geomap in Workbook. Choose to display the output of our logs as a map:  <br/>
<br />
<img src="https://i.ibb.co/grQd3mK/Image9.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/><br />
<br />
Run the Sentinel that will be the SIEM to visualise the attack data. Note attacks have already begun. The larger the size of the circle, the more people are attacking from that location:  <br/>
<br />
<img src="https://i.ibb.co/ctJHv7v/Image10.png" height="50%" width="50%" alt="Azure Sentinel SIEM"/>
 <br />
  <br />
 Thank you for reading this project.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
