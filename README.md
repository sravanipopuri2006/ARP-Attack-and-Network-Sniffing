# ARP-Attack-and-Network-Sniffing
# Explore Network Sniffing and ARP Attacks

# AIM:

To explore network sniffing and ARP Attacks

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## ARP Attacks:  
ARP spoofing: A hacker sends fake ARP packets that link an attacker's MAC address with an IP of a computer already on the LAN. 
Boot kali and Windows7 virtual machines.
In windows 7 give the command arp -a
## OUTPUT:


From kali linux issue the command :
sudo arpspoof -i eth0 -t <target system> <gateway>
## OUTPUT:
 <img width="398" height="297" alt="image" src="https://github.com/user-attachments/assets/9c3c31ad-8567-4103-910c-169f5ceedad4" />
 <br/>

A Man-in-the-Middle (MITM) attack is a type of cybersecurity attack in which an attacker secretly positions themselves between two communicating systems in order to intercept, monitor, or manipulate the exchanged data without the knowledge of either party. In local area networks, one common technique used to perform a MITM attack is ARP poisoning, also known as ARP spoofing. ARP (Address Resolution Protocol) is responsible for mapping IP addresses to MAC addresses within a network. In a penetration testing environment, tools such as Ettercap are used to simulate this attack through ARP poisoning on a local network.
<img width="783" height="367" alt="image" src="https://github.com/user-attachments/assets/2529746a-a008-4b1e-8264-8c20f4f05a24" />
<br/>
In a penetration testing laboratory setup, a Kali Linux system is commonly used as the attacker machine because it contains pre-installed security testing tools such as Ettercap. A Windows system is generally used as the victim or target machine connected to the same local network. The attack process begins by launching Ettercap with administrative privileges and selecting the correct network interface connected to the LAN. The attacker then uses the “Scan for Hosts” feature to identify active systems available on the network. Ettercap displays discovered devices such as the Windows victim machine, the network router, and other connected hosts. The penetration tester assigns the Windows system as Target 1 and the router or default gateway as Target 2, creating a communication bridge between the two systems.
<img width="786" height="372" alt="image" src="https://github.com/user-attachments/assets/b8e02d3e-8446-4128-97a7-1503dff9c099" />
<br/>
After enabling ARP poisoning, fake ARP messages are sent to both systems, causing their traffic to pass through the Kali machine. This allows the attacker to monitor or analyze network communication for security testing and educational purposes. After selecting the targets, the attacker starts the ARP poisoning process from the “MITM” section within Ettercap. The tool continuously sends fake ARP packets to both the victim system and the router. The Windows machine is tricked into believing that the Kali machine is the router, while the router is simultaneously tricked into believing that the Kali machine is the Windows system. Because of this false association, all network traffic exchanged between the victim and the gateway begins passing through the attacker system. This allows the penetration tester to capture packets, analyze network communication, monitor unencrypted data, and study network vulnerabilities in a controlled environment.
<br/>
Invoke the wireshark and examine the various menus and controls of the tool:
<br/>
<img width="794" height="373" alt="image" src="https://github.com/user-attachments/assets/1ca0fd44-6434-4b4d-9ad1-48a4969d1e5a" />





## RESULT:
The kali linux tools for ARP Attack and Network Sniffing were identified successfully
