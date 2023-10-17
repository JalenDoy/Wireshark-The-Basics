# Wireshark-The-Basics

<h2>Description</h2>

<br />

<p align="center">
<br/>
<img src="https://i.imgur.com/rzicTZa.png"/>

<h2>Packet Dissection</h2>

<p align="center">
CTF Questions <br/>
<img src="https://i.imgur.com/yQdYmTi.png"/>

**View packet number 38. Which Markup language3 is used under the HTTP protocol?**
1. To start, I will double click on the **Exercise.pcapng** file on the TryHackMe Ubuntu to launch it into **Wireshark**.
2. Next I will navigate to packet number 38 to start the pcap analysis investigation.

<p align="center">
Packet Number 38 in Wireshark <br/>
<img src="https://i.imgur.com/WflYxqR.png"/>

3. Looking at the bottom pane, under the **Hypertext Transfer Protocol** tab I can see the answer to the first questions which is **Extensible Markup Language**.

**What is the arrival date of the packet? (Answer format: Month/Day/Year)**
1. To determine this answer, click on the **Statistics** tab at the top of **Wireshark** and select **Capture File Properties**.
2. A detals window should pop up with information regarding the pcap file and under the **Time** section there is: **First Packet: 2004-05-13 10:17:07**. This is the answer.

<p align="center">
Arrival date of the packet <br/>
<img src="https://i.imgur.com/VxaOlrZ.png"/>

**What is the TTL value?**
1. Ensure that packet number 38 is selected and in the bottom pane click on **Internet Protocol Version 4**. Navigate down until you see **Time to Live: 47**. This is the answer we are looking for. 

**What is the TCP payload size?**
1. Enasure that packe number 38 is selected and in the bottom pane click on **Transmission Control Protocol**. Navigate down until you see **[TCP Segment Len: 424]**. The answer is **424**.

**What is the e-tag value?**
1. Ensure that packet number 38 is selected and in the bottom pane click on **Hypertext Transfer Protocol**. Navigate down until you see **ETAG: "9a01a-4696-7e354b00"\r\n"**. This is the answer we are looking for.

<p align="center">
CTF Answers <br/>
<img src="https://i.imgur.com/MuCYFkj.png"/>


