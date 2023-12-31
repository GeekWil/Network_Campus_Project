<h1>Network Design</h1>
 
<h2>Description</h2>
"ECI Business" is an emerging small company with a workforce of 80 employees spread across four office buildings. The company's primary site is situated in Vancouver, with additional offices located in Calgary, Montreal, and Toronto, spanning across Canada.

To support its operations effectively, the company seeks to establish a robust network infrastructure. This infrastructure should provide reliable and secure internet connectivity between the eastern and western regions, while ensuring high availability and redundancy in Vancouver.

This project encompasses the design and implementation of a comprehensive network architecture, including aspects such as network design, IP addressing, VLAN configuration, and network security measures. By addressing each of these components, the project will demonstrate how the company's specific requirements are met in terms of connectivity, reliability, and data protection.

***********This project is constrained by a total of four routers and four switches available for implementation.***********
<br />


<h2>Networking Simulation Tool</h2>

- <b>Cisco Packet tracer</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
<br />
<b>The picture shows the simple topology of the network design, "West" will be the main site containing Vancouver and Calgary, <br/> 
supporting high availability and redundancy. East will be the other site that has Montreal and Toronto</b> <br/>
<br />
  
<img src="https://i.imgur.com/UoGBPdl.png" alt="Frist topology"/>
<br />
<br />
<br />
<br />
<br />
<b>This picture shows more details about how each campus will look like</b><br/>
<img src="https://i.imgur.com/gjMwo7q.png" alt="The full topology"/>
<br />
<br />
<br />
<br />
<br />
<b>This is the detailed logical topology that includes all the IP addressing and VLAN </b><br/>
<br />
<ul>
  <li>Vancouver: Vlan 10 - 192.168.1.0/24</li>
  <li>Calgary:   Vlan 20 - 192.168.2.0/24</li>
  <li>IT (West): Vlan 30 - 192.168.3.0/24</li>
  <li>Montreal:  Vlan 40 - 192.168.4.0/25</li>
  <li>Toronto:   Vlan 50 - 192.168.4.128/26</li>
  <li>IT (East): Vlan 60 - 192.168.4.192/28</li>
</ul>

<img src="https://i.imgur.com/9FReK4J.png" alt="Detail logical topology"/>
<br />
<h3>Protocol that is used:</h3>
<ul>
  <li>OSPFv2</li>
  <li>DHCPv4, DHCPv6</li>
  <li>LACP(Between S1&S3)</li>
  <li>HSRP(Between West&West2 routers)</li>
  <li>IPSEC over GRE tunnel</li>
  <li>NTP</li>
</ul>

<br />
<br />
<br />



<h3>Simulate on Packet tracer<h3>
<img src="https://i.imgur.com/fMDg6fK.png" alt="packet tracer"/>
<br />
<br />
<br />
<br />

<b>Domain controller<b/> <br/>
<br />
<img src="https://i.imgur.com/jAOR9br.png" alt="Domain controller"/>
<br />
<br />
<br />
<br />
<br />
<br />
<b>Linux web servers, DHCP failover</b><br/>
<br />
<img src="https://i.imgur.com/cEV4RiM.png" alt="Linux servers"/>
<br />
Linux will act as a DHCP server if the router failed<br />
<br />
<br />
<br />
<br />

<!--
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
-->

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
