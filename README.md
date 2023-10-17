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



<h2>Packet Navigation</h2>

<p align="center">
CTF Questions <br/>
<img src="https://i.imgur.com/uLwsPNf.png"/>

**Search the "r4w" string in packet details. What is the name of artist 1?**
1. At the top of **Wireshark** click on **Edit** tab and then click on **Find Packet**.
2. In the search bar, ensure **String** is selected and then type in **"r4w"** and the packet with the **r4w** will be automatically selected. Scroll down until r4w appears that string is the artist name. 

<p align="center">
The line that containts the r4w string <br/>
<img src="https://i.imgur.com/1hHFyTh.png"/>

**Go to packet 12 and read the comments. What is the answer?**
1. Navigate to **packet 12** and in the bottom pane there is a tab named **Packet comments**. Click on that and a set of instructions should appear.

<p align="center">
Set of Instructions in Packet 12 <br/>
<img src="https://i.imgur.com/vUgzWFo.png"/>

2. At  the top of wireshark, click on **Go** and then **Go To Packet** and type in packet number **39765** in the top right.
3. In the bottom pane, navigate to the **JPEG File Interchange Format** section and right click on it and select **Export Packet Bytes**.
4. Name the exported file any name and save it to the Desktop or Downloads folder. Navigate to that folder and type **"md5sum [Filename]"**. The question is looking for the md5 hash but the TryHackMe instructions were not loaded so it was unclear what it was looking for. The hash is your answer.  

<p align="center">
MD5 Hash of the exported image<br/>
<img src="https://i.imgur.com/W5UZGcK.png"/>

**There is a ".txt" file inside the capture file. Find the file and read it; what is the alien's name?**
1. In **Wireshark**, click on **File** > **EExport Objects** > **HTTP** and type in **.txt**.
2. One file appears, save it to the Desktop or Downloads directory and then open it.

<p align="center">
HTTP Object List<br/>
<img src="https://i.imgur.com/Hvvz7ze.png"/>

3. Once opened, The answer will appear as **Packetmaster**.

<p align="center">
notetxt<br/>
<img src="https://i.imgur.com/Zag3ddf.png"/>

**Look at the expert info section. What is the number of warnings?**
1. In **Wireshark**, click on red circle in the bottom right which will bring up the expert information page.
2. Look at **Warning** at the top and either go into fullscreen or scroll to the right and the amount of warnings will appear. The answer is 1636.

<p align="center">
CTF Answers<br/>
<img src="https://i.imgur.com/XKxZ1TA.png"/>
