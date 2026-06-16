# TRYHACKME-Intro-to-LAN-part-4-Write-Up


# TryHackMe Room: Intro to LAN
> *Technologies and designs that power private networks.*

---

## What is a Switch and a Router?

### Switches
Switches are devices within a network designed to manage multiple endpoints like computers, printers
and any other device using an Ethernet connection. Various devices plug directly into a switch's ports.

Switches are heavily utilized in larger networks, such as Small-to-Medium Businesses (SMBs) and educational institutions, 
where there are many devices connected to the network. A switch can connect a large number of devices by offering anywhere from 4 to 64 or more ports, 
typically scaling in multiples of four.

Switches are more efficient than counterparts like hubs and repeaters. Switches can track what devices are connected to which port.
They use packet switching, meaning data is broken down into packets and sent directly to the intended target, 
which significantly reduces unnecessary network traffic.

### Routers
A router's job is simply to connect networks and pass data between them. 
Routing is the term used to describe the process of data traveling across networks. 
It involves creating paths between networks so that data can reach its destination.

Switches and routers can be connected to one another to increase the redundancy (reliability) of a network by providing multiple paths for data to take. 
If one path is down, another can be used. While this method may take longer, it ensures there is virtually no network downtime.

---

## Subnetting
Networks can range in size from small to large. Subnetting is the term given to dividing a network into smaller, miniature networks within itself.

### The Octet
An IP address is made up of four sections called octets. The same goes for a subnet mask, which is also represented as a series of four bytes (32 bits), ranging in value from 0 to 255.

*   **Network Address:** This is the IP address that sits at the very start of a subnet and is used to identify the network's existence.
*   **Host Address:** An IP address assigned to identify a specific device on the subnet.
*   **Default Gateway:** This is a specific address assigned to a device on the network (usually a router) that is capable of sending information outside of the local network to another network.

### Benefits of Subnetting
*   Efficiency
*   Security
*   Full administrative control

---

## ARP & DHCP

### ARP (Address Resolution Protocol)
ARP is the technology responsible for allowing devices to identify themselves on a local network by associating a device's MAC address (physical hardware address) with its IP address (logical network address).

Each device on a network has a local directory to store this information, which is called a cache. This cache stores the identifiers of other devices on the network.

To map these two identifiers together, devices send two types of messages:

1.  **ARP Request:** A message broadcasted on the network to other devices asking, *"Who owns this IP address, and what is your MAC address?"* Devices on the network that match that address will respond by sending back an ARP Reply.
2.  **ARP Reply:** The specific device that owns the requested IP address will respond by sending an ARP Reply containing its MAC address back to the requester. The requesting device then saves this mapping into its ARP cache for future reference.

### DHCP (Dynamic Host Configuration Protocol)
When a device connects to a network without a manual IP address, it automatically requests one from a DHCP server using a quick four-step handshake known as **DORA**.


<img width="940" height="500" alt="image-4" src="https://github.com/user-attachments/assets/a4554973-19f9-4aab-8c52-26c775b2df95" />
