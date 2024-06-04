# Investigation-Report
An incident report has been brought to your attention, help police track down a suspect utilizing logs



<h2>Description</h2>


<b>Project Overview:</b>
   - It is the spring of 2015. You are a member of the Info Security team for the Central State University of St. Martin, also known as “csusm”.  Your team receives a call from the police who explain that over the past week, someone(s) wrote a threat on one of the campus buildings.  They are concerned about safety.  They are interested in a small group of people and ask if you if there is any way to discover the locations and movements of these people during the time period of 3/14 through 3/21.

   - In this project, I go step by step in identifying "suspect 4". From initial connection to the network and trailing their movements

<b>Deliverables:</b> 
- Identify the mac address these suspects used on campus
- Discover what IP addresses were used by each of your suspects
-	Provide a record of their activities/locations on campus
- If possible, identify the devices they use

<h2>Languages and Utilities Used</h2>

- <b>Linux bash</b> 
- <b>Linux server</b>
- <b>Microsoft word</b>
- <b>Snag it</b>
- <b>Aruba wireless logs,
	Identify user MAC,
	User IP,
	Access point user connected to,
  Timestamps,
	Username<b/>

- <b>Wireshark
Identifies MAC OUI<b/>


<h2>Environments Used </h2>

- <b>Linux Kali workstation</b>
- <b>Linux remote log server</b>
- <b>Aruba wireless controller logs</b>

<h2>Most time Spent: Markstein Hall </h2>

<p align="center">
Identify network and system requirements: <br/>
<img src="https://i.imgur.com/wV6AGc9.png height="80%" width="80%" 
<br />
<br />
<p align="center">
  
<h2>Device Identification and Time Spent </h2>
<p align="center">
<img src="https://imgur.com/kJC1YXe.png" height="80%" width="80%" 
<br />
<br />
<p align="center">
  
<h2>Further investigation: <h2/>
<p align="center">
<img src="https://imgur.com/N1bYX6W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">

  <h2>Suspect's movements: <h2/>
  <img src="https://imgur.com/HrxdLfJ.png" height="80%" width="80%" />
  <br />
  <br />
</p>

<h2> Methods </h2>
- <b>The method to obtain the evidence utilizing the logs from Mar14-21. This was a collection of logs from the DHCP and wireless logs to facilitate this analysis. Utilizing Linux commands, we were able to sort and find key identifiers to our suspect.  Due to the fields not labeled or easily readable, I queried every field to get the output we were looking for.  </b>


- <b> Queries used
 - grep -w "suspect4" wireless_log_extract.txt | awk '{print $1,$2,$3,$4, $10, $11, $12, $15, $21}'
Output:
Mar 23 15:33:51 authmgr[3670]: username=suspect4 MAC=d8:cf:9c:xx:xx:xx IP=192.168.0.111 AP=MH101-8e46 auth

This provided all  fields for the information we needed, date, time, username, MAC, IP, and access point name
- I also used the Wireshark OUI identifier to identify a device by it’s MAC address. 
 </b>

<h2>Summary </h2>

- <b>In summary, Suspect 4 predominantly frequented Markstein Hall, with secondary activity concentrated in Academics and University Hall. Their ingress and egress patterns suggest a focal point near the parking lot adjacent to the Markstein building. Suspect 37, on the other hand, was primarily active in ACD, USU, Arts, and Markstein areas. Their journey culminated at the University Student Union, as evidenced by their final logged activities.
Through thorough analysis of captured logs, we have developed the capability to precisely track the suspects' movements and pinpoint their locations at any given time duration. </b>

<p align="center">
 

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
