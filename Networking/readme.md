## Table of Content:
- [Networking](#networking)
- [What Is the OSI Model](#what-is-the-osi-model)
- [Layer 1 - Physical layer](#layer-1---physical-layer)
- [Layer 2 - Data link layer](#layer-2---data-link-layer)
- [Layer 3 - Network layer](#layer-3---network-layer)
- [Decimal to Binary Conversion (IP Addressing)](#decimal-to-binary-conversion-ip-addressing)
  - [Converting decimal to Binary `133.33.33.7`](#converting-decimal-to-binary-13333337)
    - [Following the method above you continue for 133.**33.33.7** to get :](#following-the-method-above-you-continue-for-13333337-to-get-)
- [Layer 4\&5 - Session \& Transport layers](#layer-45---session--transport-layers)
  - [Segments](#segments)
- [Network Address Translation (NAT)](#network-address-translation-nat)
  - [](#)
# Networking

- Networking is a fundamental component of DevOps practices
   - enabling seamless **communication** 
   -  **collaboration** between development, operations, and other stakeholders.
- DevOps engineers play a crucial role in ensuring that networking
infrastructure:
  - supports the **continuous integration, delivery, and deployment** 
  -  **optimize** application performance
  - **Enhance security**
   - **Troubleshoot** issues effectively. 
  
# What Is the OSI Model
The Open Systems Interconnection (OSI) model describes seven layers that computer systems use to communicate over a network.

![OSI-7-layers](images/OSI-7-layers.jpg)

# Layer 1 - Physical layer

- The Physical Layer serves as the foundation of the OSI Model, focusing on the actual transmission of data in its raw bit form over a physical medium. Focuses on the physical shared medium 
- standard for transmitting and receiving from the medium 
-  The Physical Layer doesn't define any particular meaning for those signals other than the basic binary values 0 and 1.
<br>

![layer1](images/layer1.png)

- Layer1 has **ONE** broadcast and **ONE** division main : Layer 1 networks don't scale very well. Has higher chance of collisions and data corruption as it RE- TRANSMITS EVERYTHING
  
> [!IMPORTANT]  
> **No access control <br>
> No uniquely identified devices  <br>
> No device => device communications**


#  Layer 2 - Data link layer

-  Layer two relies on functional layer one networks, which provide various capabilities to higher layers.
-   Layer one handles the physical transmission and reception of frames while **layer two provides them for communication.**
     ## Framing
    - One of the key functions of the Data Link Layer is to divide the stream of bits received from the Physical Layer into manageable frames
    - Framing allows devices to recognize the start and end of each transmission.
    -  This process ensures that data is correctly segmented for transmission over the network.
      ## Network devices
     - The Data Link Layer is crucial for the operation of network devices like switches
     - use MAC addresses to determine how to forward frames
     - This capability enables switches to efficiently direct data only to the specific port where the destination device is connected, **minimizing network congestion and enhancing overall network performance**
      ## Mac Adress:
     - MAC addresses are unique identifiers assigned to network interface cards (NICs) or network adapters.  48-bit long  `00:1b:63:84:45:e6`. These addresses are used to identify devices on a local network segment.
     - When a device wants to send data to another device within the same network, it uses the recipient's MAC address to direct the frame to the correct destination.
     -  The Data Link Layer is **responsible for adding the MAC address information to the frame's header.**
  <br>

  ![Layer2](images/layer2.png)

  > [!IMPORTANT]  
> This layer is responsible for node-to-node communication and error detection <br>
> 
>  It organizes data into frames, adds physical addresses (MAC addresses) to these frames, and ensures reliable transmission over the physical layer  <br>
> 
> Ethernet is a common example of a protocol operating at this layer. <br>
> **Contains COLLISION detection**

![layer2_datalink](images/layer2_datalink.png)
<br>


# Layer 3 - Network layer

-  This layer enables devices to communicate across different networks by routing data packets. It's where logical addressing, like IP addresses, comes into play. 
-  Routers operate at this layer, using logical addresses to make decisions about how to forward packets towards their destination. 
 -  It's responsible for determining the best path for data to travel across interconnected networks.
  
     ## Routing Packet and Packet forwarding
       - One of the fundamental tasks of the Network Layer is to route data packets from the sender to the receiver.
       -  It accomplishes this by determining the most efficient path for data to travel through a complex network topology.
       -  As data packets traverse the network, the Network Layer handles **packet forwarding**.
       -  This involves inspecting the destination IP address in each packet's header and determining the next hop (next network device) on the route to the destination.
       -   The Network Layer also manages the encapsulation and decapsulation of data packets for transmission and reception.
  
     ## Error Handling 
       - While the primary responsibility for error handling lies with higher layers, the Network Layer may perform basic error detection and reporting.
      -  If a packet is found to be corrupt or undeliverable, **the Network Layer may discard it or request retransmission.**
  
     ## Logical Addressing
       - Each device on a network is assigned a unique address known as an IP (Internet Protocol) address.
       -  IP addresses, both IPv4 and IPv6, are used for identifying devices and their network location.
       -  Responsible for managing these addresses, which are used for source and destination identification in data packets.
   
     ## Inter-Network Communication
       - The Network Layer is crucial for enabling communication between different networks. 
       - It acts as the boundary where data moves between local area networks (LANs) and wide area networks (WANs).
       -  Routers, which operate at this layer, play a central role in **connecting disparate networks and ensuring data can traverse these boundaries.**
  
  ![layer3](images/layer3.png)

  > [!IMPORTANT]  
>  - The network layer handles moving data **from the SOURCE to the destination**. <br>
>  - It's responsible for logical addressing (like IP addresses), packet forwarding, and traffic control.  <br>
> - Routers operate at this layer to determine the best path for data to travel across interconnected networks. <br>
> - Allows for Device <=> Device communication over the internet
> - Provides **NO** method for channels of communication <br>
> - Can be delivered out of order ..



# Decimal to Binary Conversion (IP Addressing)
  - Decimal to binary conversion in IP addressing involves transforming the standard decimal notation of an IP address into its binary equivalent. 
  - This conversion is essential for computers to understand and process IP addresses, as they communicate in binary format at the network level. 
  
![](images/decimal-binary.png)

   ## Converting decimal to Binary `133.33.33.7`

![](images/decimal-binary-conversion.png)



### Following the method above you continue for 133.**33.33.7** to get : 

![](images/conversion%20.png)


# Layer 4&5 - Session & Transport layers 
-  The Transport Layer (Layer 4) ensures reliable end-to-end communication and data delivery across networks. 
-  It segments data into manageable pieces, manages flow control to prevent congestion, detects and corrects errors, and multiplexes multiple data streams. 
-  It supports both **connection-oriented (TCP) and connectionless (UDP)** communication, vital for various applications like web browsing and real-time communication.
   - **TCP is slower but more reliable**
   - **UDP is Faster but Less reliable**  <br>
  
*Both use IP as transit, TCP just offers a more reliable  connection while UDP is all about performance*


   ## Segments
   - One of the key roles of the Transport Layer is to divide large messages into smaller segments, making them easier to transmit across the network.
   - These segments are typically referred to as “packets” or “datagrams.”
   - Segmenting data is especially important when the message is too large to fit into a single network packet.
  
> [!IMPORTANT]  
>The Transport Layer allows for multiple services to run simultaneously on a single device, supporting various applications and facilitating secure data transfer over encrypted connections.


- The Session Layer (Layer 5):
   -  establishes
   -  maintains 
   -  terminates communication sessions between devices.
-  It **ensures synchronized and reliable data exchange**, handles session setup and termination, manages dialog control to prevent conflicts, and implements synchronization points and checkpointing for resuming interrupted sessions. 
-  It's crucial for applications like file transfer, remote desktop connections, and online gaming, where maintaining a seamless user experience is essential.
-  


# Network Address Translation (NAT)

- NAT is designed to overcome **IPv4 shortages**
- To give internet access to private devices we need to use Network Address Translation (NAT)
   - Translates **Private** IPv4 address to** Public**
- NAT also provides some security benefits 
  
   ## 
   - 