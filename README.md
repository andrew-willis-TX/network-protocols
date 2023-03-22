<h1> Network Protocols and Traffic Observation</h1>
<h2> Environment and Technology </h2>  

- Microsoft Azure
- Windows 10 VM
- Ubunutu VM
- Wireshark  

<h2> Setup/Configuration Steps </h2>

1. Create a Windows 10 VM
2. Create and Ubunut VM. Make sure it is in the same reource group and virtual network as the Windows 10 VM
3. Check topology in Azure Network Watcher to verify both machines are on the same network.
4. Use Remote Desktop to log in to the Windows 10 VM
5. Install Wireshark on Windows 10 VM
6. From the Windows 10 VM, ping the private IP address of the Ubunut VM
7. Open Wireshark and filter for ICMP traffic.
8. Observe the ping requests and replies within wireshark. 
9. From the Windows 10 VM, use command line to ping a public website such as google.com.
10. Observe the traffic in Wireshark
11. Use command line on Windows 10 VM to perpetually ping ("ping -t private ip") the Ubunutu VM.
12. Within the Ubuntu VM, open Network Security Groups and disable all inbound ICMP traffic
13. Within the Windows 10 VM, observe the ICMP traffic and command line activity
14. Within the Ubuntu VM, re-enable inbound ICMP traffic.
15. Within the Windows 10 VM, observe the ICMP traffic and command line activity. Then, end the ping ("ctrl + c").
16. Within Wireshark, filter for DHCP traffic only
17. Within the Windows 10 VM, attempt to issue the Ubuntu VM a new IP Address from the command line ("ipconfig /renew"). Observe the traffic in Wireshark.
18. Within the Windows 10 VM, filter Wireshark for DNS traffic.
19. Within the Windows 10 VM, use command line ("nslookup") to check the IP address of a few public websites. Observe the DNS traffic in Wireshark.
20. Within the Windows 10 VM, filter Wireshark for RDP traffic (tcp port == 3389. Observe the immediate and non-stop traffic
21. Close Remote Desktops and delete Azure resources
 

