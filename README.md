<h1> Network Protocols and Traffic Observation</h1>
<p align="center">
<img src="https://abouconde335669239.files.wordpress.com/2018/12/imagesa040026w.png" height="25%" width="25%" alt="Network Security Group Logo"/>
</p>

<h2> Environment and Technology </h2>  

- Microsoft Azure
- Windows 10 VM
- Ubunutu VM
- Wireshark  

<h2> Setup/Configuration Steps </h2>

1. Create a Windows 10 VM.  
<p align="center">
<img src="https://i.imgur.com/5InKzKl.png" height="50%" width="50%" alt="Creating a Windows 10 VM"/>
</p>

2. Create an Ubuntu VM. Make sure it is in the same reource group and virtual network as the Windows 10 VM.
<p align="center">
<img src="https://i.imgur.com/FQH71iM.png" height="50%" width="50%" alt="Creating an Ubuntu VM"/>

3. Check topology in Azure Network Watcher to verify both machines are on the same network.
<p align="center">
<img src="https://i.imgur.com/vtjYqYD.png" height="50%" width="50%" alt="Checking the Virtual Network topology"/>

4. Use Remote Desktop to log in to the Windows 10 VM.
<p align="center">
<img src="https://i.imgur.com/5etBbcu.png" height="50%" width="50%" alt="Logging in to VM1 through Remote Desktop."/>
</p>

5. Install Wireshark on Windows 10 VM. Use the default installation settings.
<p align="center">
<img src="https://i.imgur.com/pfWJcrF.png" height="50%" width="50%" alt="Installing Wireshark Protocol Analyzer"/>

6. From the Windows 10 VM, using PowerShell, ping the private IP address of the Ubuntu VM. 
<p align="center">
<img src="https://i.imgur.com/bIaHPPd.png" height="50%" width="50%" alt="Pinging VM2's private IP from VM1."/>
</p>

7. Open Wireshark and filter for ICMP traffic.
<p align="center">
<img src="https://i.imgur.com/fPTdFpb.png" height="50%" width="50%" alt="Filtering Wireshark to show ICMP traffic only"/>
</p>

8. Observe the ping requests and replies within Wireshark. 
<p align="center">
<img src="https://i.imgur.com/tvUfkbU.png" height="50%" width="50%" alt="ICMP traffic showing due to ping we sent from PowerSehll."/>
</p>

9. From the Windows 10 VM, use PowerShell to ping a public website such as google. Observe the traffic in Wireshark.  
<p align="center">
 <img src="https://i.imgur.com/pdRiJUj.png" height="50%" width="50%" alt="Observing ICMP traffic from google ping."/>
 </p>
 
10. Use PowerShell on Windows 10 VM to perpetually ping ("ping -t private ip") the Ubunutu VM.
<p align="center">
 <img src="https://i.imgur.com/tJxdj75.png" height="50%" width="50%" alt="Observe the traffic from the perpetual ping command."/>
 </p>
 
11. Within the Ubuntu VM, open Network Security Groups and disable all inbound ICMP traffic
14. Within the Windows 10 VM, observe the ICMP traffic and command line activity
15. Within the Ubuntu VM, re-enable inbound ICMP traffic.
16. Within the Windows 10 VM, observe the ICMP traffic and command line activity. Then, end the ping ("ctrl + c").
17. Within Wireshark, filter for DHCP traffic only
18. Within the Windows 10 VM, attempt to issue the Ubuntu VM a new IP Address from the command line ("ipconfig /renew"). Observe the traffic in Wireshark.
19. Within the Windows 10 VM, filter Wireshark for DNS traffic.
20. Within the Windows 10 VM, use command line ("nslookup") to check the IP address of a few public websites. Observe the DNS traffic in Wireshark.
21. Within the Windows 10 VM, filter Wireshark for RDP traffic (tcp port == 3389. Observe the immediate and non-stop traffic
22. Close Remote Desktops and delete Azure resources
 

