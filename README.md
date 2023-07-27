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
Network Tracker: <br/>
<br />
<img src="https://i.ibb.co/tcc9nNr/Image0.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
<br />
First, I captured some network traffic using Wireshark. I created a pcap file. This file consisted of all network traffic going to and from my laptop. To initialise the capture, I selected an interface that the traffic is going through. <br/>
<br />
<img src="https://i.ibb.co/FDpRYNQ/Image1.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
After capturing packets, I exported them in pcap format . <br/>
<br />
<img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*mcmjDxqGX03hDW-QA2-eJg.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
  <br />
Next was to implement code. A variable is declared with the GeoLiteCity database. The main method will open the captured data along with creating the header and footer of the KML file, which is the output file that will be uploaded to Google Maps. Next I added a method that looped over the captured network data and extracted the IP’s. The application will loop over our pcap data and extract source and destination IP adresses of each captured network packet. The IP addresses can’t be used alone as input to Google Maps, the code needs to attach a Geo location.  <br/>
<br />
<img src="https://i.ibb.co/Fnwwjd1/Image3.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
After the KML file is created from Python, we create a new map at www.google.com/mymaps/. A new layer is imported with the KML file previously created. <br/>
<br />
<img src="https://i.ibb.co/TKzTpN8/Image4.png" height="50%" width="50%" alt="Network Tracker"/>
<br />
Once the file is uploaded, the network traffic from the captured data will be dislayed on the map.<br/>
<br />
<img src="https://i.ibb.co/CPdPFHS/Image5.png" height="50%" width="50%" alt="Network Tracker"/>
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
