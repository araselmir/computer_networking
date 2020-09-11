# (A). Layers of OSI Model
<h2>OSI Model</h2>
<p>The Open Systems Interconnection (OSI) model is a conceptual model created by the International Organization for Standardization which enables diverse communication systems to communicate using standard protocols. In plain , the OSI provides a standard for different computer systems to be able to communicate with each other.</p>
<h2>OSI Layers</h2>
There are 7 Layers of OSI Model.

![Screenshot from 2020-09-10 16-05-45](https://user-images.githubusercontent.com/62602944/92715683-a1d97280-f37f-11ea-9004-8e0bd16f6ab6.png)


<h2> Layer architecture</h2>

<table class="wikitable" style="margin: 1em auto 1em auto;">
<tbody><tr>
<th colspan="3">Layer
</th>
<th>Protocol data unit (PDU)
</th>
<th>Function
</th></tr>
<tr>
<th rowspan="4">Host<br>layers
</th>
<td style="background:#d8ec9b;">7
</td>
<td style="background:#d8ec9b;">Application
</td>
<td style="background:#d8ec9c;" rowspan="3">Data
</td>
<td style="background:#d8ec9c;">High-level APIs, including resource sharing, remote file access
</td></tr>
<tr>
<td style="background:#d8ec9b;">6
</td>
<td style="background:#d8ec9b;">Presentation
</td>
<td style="background:#d8ec9b;">Translation of data between a networking service and an application; including character encoding, data compression and encryption/decryption
</td></tr>
<tr>
<td style="background:#d8ec9b;">5
</td>
<td style="background:#d8ec9b;">Session
</td>
<td style="background:#d8ec9b;">Managing communication sessions, i.e., continuous exchange of information in the form of multiple back-and-forth transmissions between two nodes
</td></tr>
<tr>
<td style="background:#e7ed9c;">4
</td>
<td style="background:#e7ed9c;">Transport
</td>
<td style="background:#e7ed9c;">Segment, Datagram
</td>
<td style="background:#e7ed9c;">Reliable transmission of data segments between points on a network, including segmentation, acknowledgement and multiplexing
</td></tr>
<tr>
<th rowspan="3">Media<br>layers
</th>
<td style="background:#eddc9c;">3
</td>
<td style="background:#eddc9c;">Network
</td>
<td style="background:#eddc9c;">Packet
</td>
<td style="background:#eddc9c;">Structuring and managing a multi-node network, including addressing, routing and traffic control
</td></tr>
<tr>
<td style="background:#e9c189;">2
</td>
<td style="background:#e9c189;">Data link
</td>
<td style="background:#e9c189;">Frame
</td>
<td style="background:#e9c189;">Reliable transmission of data frames between two nodes connected by a physical layer
</td></tr>
<tr>
<td style="background:#e9988a;">1
</td>
<td style="background:#e9988a;">Physical
</td>
<td style="background:#e9988a;">Bit, Symbol
</td>
<td style="background:#e9988a;">Transmission and reception of raw bit streams over a physical medium
</td></tr></tbody></table>

<h3>7. The application Layer</h3>
<p>This is the only layer that directly interacts with data from the user. Software applications like web browsers and email clients rely on the application layer to initiate communications. But it should be made clear that client software applications are not part of the application layer; rather the application layer is responsible for the protocols and data manipulation that the software relies on to present meaningful data to the user. Application layer protocols include HTTP as well as SMTP (Simple Mail Transfer Protocol is one of the protocols that enables email communications).</p>

![Screenshot from 2020-09-10 16-33-46](https://user-images.githubusercontent.com/62602944/92718976-5a091a00-f384-11ea-92c4-36e43389c263.png)

<h3>6. The Presentation Layer</h3>
<p>This layer is primarily responsible for preparing data so that it can be used by the application layer; in other words, layer 6 makes the data presentable for applications to consume. The presentation layer is responsible for translation, encryption, and compression of data.</p>
<p>Two communicating devices communicating may be using different encoding methods, so layer 6 is responsible for translating incoming data into a syntax that the application layer of the receiving device can understand.</p>
<p>If the devices are communicating over an encrypted connection, layer 6 is responsible for adding the encryption on the sender’s end as well as decoding the encryption on the receiver's end so that it can present the application layer with unencrypted, readable data.</p>
<p>Finally the presentation layer is also responsible for compressing data it receives from the application layer before delivering it to layer 5. This helps improve the speed and efficiency of communication by minimizing the amount of data that will be transferred.</p>

![Screenshot from 2020-09-10 16-33-50](https://user-images.githubusercontent.com/62602944/92718990-5d9ca100-f384-11ea-8ab3-16ed0fb50606.png)

<h3>5. The Session Layer</h3>
<p>This is the layer responsible for opening and closing communication between the two devices. The time between when the communication is opened and closed is known as the session. The session layer ensures that the session stays open long enough to transfer all the data being exchanged, and then promptly closes the session in  to avoid wasting resources.</p>
<p>The session layer also synchronizes data transfer with checkpoints. For example, if a 100 megabyte file is being transferred, the session layer could set a checkpoint every 5 megabytes. In the case of a disconnect or a crash after 52 megabytes have been transferred, the session could be resumed from the last checkpoint, meaning only 50 more megabytes of data need to be transferred. Without the checkpoints, the entire transfer would have to begin again from scratch.</p>
  
  
  ![Screenshot from 2020-09-10 16-33-54](https://user-images.githubusercontent.com/62602944/92719002-61c8be80-f384-11ea-8702-2a7e425fbe5f.png)
  
  <h3>4. The Transport Layer</h3>
  <p>Layer 4 is responsible for end-to-end communication between the two devices. This includes taking data from the session layer and breaking it up into chunks called segments before sending it to layer 3. The transport layer on the receiving device is responsible for reassembling the segments into data the session layer can consume.</p>
  <p>The transport layer is also responsible for flow control and error control. Flow control determines an optimal speed of transmission to ensure that a sender with a fast connection doesn’t overwhelm a receiver with a slow connection. The transport layer performs error control on the receiving end by ensuring that the data received is complete, and requesting a retransmission if it isn’t.</p>
  
  ![Screenshot from 2020-09-10 16-33-57](https://user-images.githubusercontent.com/62602944/92719020-67260900-f384-11ea-8bbd-83984b6e5d02.png)

<h3>3. The Network Layer</h3>
<p>The network layer is responsible for facilitating data transfer between two different networks. If the two devices communicating are on the same network, then the network layer is unnecessary. The network layer breaks up segments from the transport layer into smaller units, called packets, on the sender’s device, and reassembling these packets on the receiving device. The network layer also finds the best physical path for the data to reach its destination; this is known as routing.</p>

![Screenshot from 2020-09-10 16-34-00](https://user-images.githubusercontent.com/62602944/92719036-6db48080-f384-11ea-9fed-34d5361a7a9a.png)

<h3>2. The Data Link Layer</h3>
<p>The data link layer is very similar to the network layer, except the data link layer facilitates data transfer between two devices on the SAME network. The data link layer takes packets from the network layer and breaks them into smaller pieces called frames. Like the network layer, the data link layer is also responsible for flow control and error control in intra-network communication (The transport layer only does flow control and error control for inter-network communications).</p>

![Screenshot from 2020-09-10 16-34-02](https://user-images.githubusercontent.com/62602944/92719060-72793480-f384-11ea-9232-7803e88a3e7b.png)

<h3>1. The Physical Layer</h3>
<p>This layer includes the physical equipment involved in the data transfer, such as the cables and switches. This is also the layer where the data gets converted into a bit , which is a string of 1s and 0s. The physical layer of both devices must also agree on a signal convention so that the 1s can be distinguished from the 0s on both devices.</p>

![Screenshot from 2020-09-10 16-34-06](https://user-images.githubusercontent.com/62602944/92719074-75742500-f384-11ea-81d8-95ff38a12fd9.png)


# (B). TCP/IP(Transmission Control Protocol/Internet Protocol)
<h2> What is TCP/IP ?</h2>
<p>TCP/IP, or the Transmission Control Protocol/Internet Protocol, is a suite of communication protocols used to interconnect network devices on the internet. TCP/IP can also be used as a communications protocol in a private computer network (an intranet or an extranet).</p>
<p>IP is a connectionless protocol, which means that each unit of data is individually addressed and routed from the source device to the target device, and the target does not send an acknowledgement back to the source. That’s where protocols such as the Transmission Control Protocol (TCP) come in. TCP is used in conjunction with IP in  to maintain a connection between the sender and the target and to ensure packet .</p>
<h2>Why called TCP/IP ?</h2>
<p>When the protocols were first implemented, there was no IP, only TCP, which then stood for Transmission Control Program. Jon Postel recognized in 1977 that a monolithic protocol was a bad design and the responsibilities of the original protocol were split into layers. The new implementation was called TCP/IP.</p>
<h2>What does TCP/IP do, exactly? And how does it work?</h2>
<p>TCP/IP was developed by the U.S. Department of Defense to specify how computers transfer data from one device to another. TCP/IP puts a lot of emphasis on accuracy, and it has several steps to ensure that data is correctly transmitted between the two computers.</p>
<p>Here’s one way it does that. If the system were to send the whole message in one piece, and if it were to encounter a problem, the whole message would have to be re-sent. Instead, TCP/IP breaks each message into packets, and those packets are then reassembled on the other end. In fact, each packet could take a different route to the other computer, if the first route is unavailable or congested.</p>
<p>

![What_is_TCP-IP](https://user-images.githubusercontent.com/62602944/92774181-07008880-f3bf-11ea-87be-14d8d4b9ac69.png)

<h2>Layers of the TCP/IP model</h2>
<p>There are 4 layers of the TCP/IP model</p>
<h3>1. Application layer</h3>
<p>The application layer provides applications with standardized data exchange. Its protocols include the HTTP, FTP,  Protocol 3 (POP3), Simple Mail Transfer Protocol (SMTP) and Simple Network Management Protocol (SNMP). At the application layer, the payload is the actual application data.</p>
<h3>2.Transport layer</h3>
<p>The transport layer is responsible for maintaining end-to-end communications across the network. TCP handles communications between hosts and provides flow control, multiplexing and reliability. The transport protocols include TCP and User Datagram Protocol (UDP), which is sometimes used instead of TCP for special purposes.</p>
<h3>3.Network layer</h3>
</p>The network layer, also called the internet layer, deals with packets and connects independent networks to transport the packets across network boundaries. The network layer protocols are the IP and the Internet Control Message Protocol (ICMP), which is used for error reporting.</p>
<h3>4.Physical layer</h3>
<p>The physical layer, also known as the network interface layer or data link layer, consists of protocols that operate only on a link -- the network component that interconnects nodes or hosts in the network. The protocols in this lowest layer include Ethernet for local area networks (LANs) and the Address Resolution Protocol (ARP).</p>

# (C).Difference between IPV4 vs IPV6

<h2>KEY DIFFERENCE</h2>
<p>1. IPv4 is 32-Bit IP address whereas IPv6 is a 128-Bit IP address.</p>
<p>2. IPv4 format is four Octect and IPv6 is 8 block Hexadecimal.</p>
<p>3. IPv4 binary bits are separated by a dot(.) whereas IPv6 binary bits are separated by a colon(:).</p>
<p>4. IPv4 is a numeric addressing method whereas IPv6 is an alphanumeric addressing method.</p>
<p>5. IPv4 supports broadcast whereas IPv6 doesn’t support broadcast.</p>
<p>6. IPv6 supports bigger payload than IPv4.</p>
<p>7. IPv4 supports VLSM (Virtual Length Subnet Mask) whereas IPv6 doesn’t support VLSM.</p>

# (D).DHCP (Dynamic Host Configuration Protocol)
<h2>What is DHCP?</h2>
<p>DHCP stands for dynamic host configuration protocol and is a network protocol used on IP networks where a DHCP server automatically assigns an IP address and other information to each host on the network so they can communicate efficiently with other endpoints.</p>
<h2>How DHCP work ?</h2>

![csg66-01-how-dhcp-works](https://user-images.githubusercontent.com/62602944/92783427-9316ae00-f3c7-11ea-9f1b-3d054bf9af28.png)

<h3>1. DHCP discovery</h3>
<p>When you start a device, the device checks whether a valid IP configuration is available on the device or not. If the valid IP configuration is not available, the device generates a special message known as <b>DHCPDISCOVER</b> and broadcasts this message on the local LAN segment.</p>
<p>To broadcast <b>DHCPDISCOVER</b> messages, the device uses the 0.0.0.0 and 255.255.255.255 as the source address and destination address, respectively.</p>
<p>The 0.0.0.0 and 255.255.255.255 are two special addresses. Any device, whether it has a valid IP configuration or not, can use these addresses to send local broadcast messages.</p>
<p>From these addresses, the 0.0.0.0 is used as the source address. If a device does not have the source address, it can use this address to send broadcast messages. 255.255.255.255 is the local broadcast address. Any message sent on this address is received by all hosts of the local network.</p>
<h3>DHCP offer</h3>
<p>Since the client sends the <b>DHCPDISCOVER</b> message to the local broadcast address, if a DHCP server is configured on the local network, it will also receive the message. If multiple DHCP servers are configured on the local network, they all will receive the <b>DHCPDISCOVER</b> message.</p>
<p>If multiple DHCP servers are available, based on their configuration, one of them or all of them can reply to the <b>DHCPDISCOVER</b> message. In reply to the <b>DHCPDISCOVER</b> message, a DHCP server sends a <b>DHCPOFFER</b> message to the client.</p>
<p>Since the client does not have an IP address, the DHCP server cannot send the DHCPOFFER message directly to the client. Because of this, the server sets the destination address to 255.255.255.255. In other words, the server also broadcasts the DHCPOFFER message to the local network.</p>
<p>The <b>DHCPOFFER</b> message includes the following important information: IP address of the client, subnet mask of the segment, IP address of the default gateway, DNS domain name, DNS server address or addresses, and TFTP server address or addresses.</p>
<p><em>Apart from these, the <b>DHCPOFFER</b> message also contains other protocol-specific information such as the lease duration and client ID. This information is required by the core functions of DHCP.</em></p>

<h3>DHCP request</h3>
<p>All hosts in the local network receive the <b>DHCPOFFER</b> message. The host that sent the <b>DHCPDISCOVER</b> message accepts the <b>DHCPOFFER</b> message. Except the original host, all other hosts ignore the <b>DHCPOFFER</b>.</p>
<p>The <b>DHCPDISCOVER</b> message contains the host's MAC address. When a DHCP server broadcasts a <b>DHCPOFFER</b> message, it also includes the host's MAC address in a parameter known as the client ID. When hosts receive the <b>DHCPOFFER</b> message, they  the client ID field in the message. If a host sees its MAC address in the client ID field, the host knows that the message is meant for it. If a host sees the MAC address of another host in the client ID field, the host knows that the message is not intended for it.</p>
<p>Depending on the number of DHCP servers, a host may receive multiple <b>DHCPOFFER</b> messages. If a host receives multiple <b>DHCPOFFER</b> messages, it accepts only one message and tells the corresponding server with a <b>DHCPREQUEST</b> message that it wants to use the offered IP configuration.</p>
<p>If only one DHCP server is available and the provided IP configuration conflicts with the client’s configuration, the client can respond with a <b>DHCPDECLINE</b> message. In this situation, the DHCP server offers another IP configuration.</p>
<p>If only one DHCP server is available and the provided IP configuration conflicts with the client’s configuration, the client can respond with a <b>DHCPDECLINE</b> message. In this situation, the DHCP server offers another IP configuration.</p>
<p>When DHCP servers receive the <b>DHCPREQUEST</b> message, besides the server whose offer has been accepted, all other servers withdraw any offers that they might have made to the client and return the offered address to the pool of available addresses.</p>
<p>The DHCPREQUEST message contains a Transaction ID field. Just like hosts use the client ID field of the <b>DHCPOFFER</b> message to know whether the message is intended for them or not, DHCP servers use the Transaction ID field of the <b>DHCPREQUEST</b> message to know whether their offer has been accepted or not.</p>

<h3>DHCP acknowledgment</h3>
<p>When the DHCP server receives a <b>DHCPREQUEST</b> message from the client, the configuration process enters its final stage. In this stage, the server sends a DHCPACK message to the client.</p>
<p>The <b>DHCPACK</b> message is an acknowledgment to the client indicating that the DHCP server has received the <b>DHCPREQUEST</b> message of the client, and the client can use the offered IP configuration.</p>
<p>In some cases, the server may also respond with a <b>DHCPNACK</b> message. The <b>DHCPNACK</b> message tells the client that the offer is no longer valid and the client needs to request an IP configuration again. Typically, this occurs when the client takes too long to respond with a <b>DHCPREQUEST</b> message after receiving a <b>DHCOFFER</b> message from the server. In such a case, the client can make a new request for another IP configuration.</p>
<p>The following image shows the above steps.</p>

![csg66-02-four-functions-of-dhcp](https://user-images.githubusercontent.com/62602944/92786393-05888d80-f3ca-11ea-9a40-bf7192e76175.png)

# (E). Loopback Interface
<h2>What is loopback interface ? </h2>
<p>The loopback interface is a virtual interface that is always up and available after it has been configured. Note that the loopback interface is not tied to the address 127.0.0.1. It’s an interface like any other, and can be assigned its own address. A loopback interface is often used as a termination address for some routing protocols, because it never goes down.</p>
<p>Another common use of a loopback address is to identify a router. For example, say you want to find out whether a particular router is up. You know that the router has an ethernet0 interface with an IP address of 10.10.1.1. You ping 10.10.1.1 and don’t get a response. Does this mean your router is down? It’s possible that the router is up and that the ping reached the router on another interface, but you didn’t receive a response because ethernet0 is down. To find out unambiguously whether the router is alive, you have to ping another interface. But that interface might be down, causing the same scenario to occur. To avoid this problem, you can configure the router’s loopback interface with a unique address. Then, when you want to telnet or ping your router, use the loopback interface’s IP address. This method ensures that you will get a response no matter how your packets reach the router.</p>
<p>Here’s how to assign an IP address to a loopback interface:</p>
<pre class="programlisting">interface loopback 0
  ip address 10.10.1.2 255.255.255.255</pre>
  
  # (F). Latency
  <h2>What is latency ?</h2>
  <p>Latency is the time that passes between a user action and the resulting response. Network latency refers specifically to delays that take place within a network, or on the Internet. In practical terms, latency is the time between a user action and the response from the website or application to this action – for instance, the delay between when a user clicks a link to a webpage and when the browser displays that webpage.</p>
  
  ![Screenshot from 2020-09-11 09-04-55](https://user-images.githubusercontent.com/62602944/92850214-fc211480-f40d-11ea-8646-bbfa76a0df5b.png)

<h2>Network latency effects on application performance</h2>
<p>Providing the storage network with sufficient bandwidth is a necessary, but not sufficient, step to ensuring good performance of a storage networking application. If excessive network latency is causing the application to spend a large amount of time waiting for responses from a distant data center, then the bandwidth may not be fully utilized, and performance will suffer.</p>
<p>Good network design can minimize node delay and congestion delay, but a law of physics governs propagation delay: the speed of light. Still, there are ways to seemingly violate this physical law and decrease the overall amount of time that applications spend waiting to receive responses from remote sites.</p>
<p>The first is credit spoofing. As described previously, credit spoofing switches can convince Fibre Channel switches or end systems to forward chunks of data much larger than the amount that could be stored in their own buffers. The multiprotocol switches continue to issue credits until their own buffers are full, while the originating Fibre Channel devices suppose that the credits arrived from the remote site.</p>
<p>Since the far-end switches also have large buffers, they can handle large amounts of data as it arrives across the network from the sending switch. As a result, fewer control messages need to be sent for each transaction and less time is spent waiting for the flow control credits to travel end to end across the high-latency network. That, in turn, increases the portion of time spent sending actual data and boosts the performance of the application.</p>
<p>Another way to get around the performance limitations caused by network latency is to use parallel sessions or flows. Virtually all storage networks operate with multiple sessions, so the aggregate performance can be improved simply by sending more data while the applications are waiting for the responses from earlier write operations. Of course, this has no effect on the performance of each individual session, but it can improve the overall performance substantially.</p>

# (G).CIDR (Classless Inter-Domain Routing)
<h2>What is CIDR (Classless Inter-Domain Routing)?</p>
<p>Classless Inter-Domain Routing (CIDR) is a standard created by the Internet Engineering Task Force in 1993 that helps to more efficiently allocate IP addresses and allows for a flexible and simplified way to identify IP addresses and route network traffic. </p>
<h2>Background of CIDR</h2>
<p>An IP address is interpreted as composed of two parts: a network-identifying prefix followed by a host identifier within that network. In the previous classful network architecture, IP address allocations were based on the bit boundaries of the four octets of an IP address. An address was considered to be the combination of an 8, 16, or 24-bit network prefix along with a 24, 16, or 8-bit host identifier respectively. Thus, the smallest allocation and routing block contained only 256 addresses—too small for most enterprises, and the next larger block contained 65536 addresses—too large to be used efficiently even by large organizations. This led to inefficiencies in address use as well as inefficiencies in routing, because it required a large number of allocated class-C networks with individual route announcements, being geographically dispersed with little opportunity for route aggregation.</p>
<p>During the first decade of the Internet after the invention of the Domain Name System (DNS) it became apparent that the devised system based on the classful network scheme of allocating the IP address space and the routing of IP packets was not scalable. This led to the successive development of subnetting and CIDR. The network class distinctions were removed, and the new system was described as being classless, with respect to the old system, which became known as classful. In 1993, the Internet Engineering Task Force published a new set of standards to define this new concept of allocation of IP address blocks and new methods of routing IPv4 packets. An updated version of the specification was published as RFC 4632 in 2006.</p>
<p>Classless Inter-Domain Routing is based on variable-length subnet masking (VLSM), which allows a network to be divided into variously sized subnets, providing the opportunity to size a network more appropriately for local needs. Variable-length subnet masks are mentioned .Accordingly, techniques for grouping addresses for common operations were based on the concept of cluster addressing, first proposed by Carl-Herbert Rokitansky.</p>

<h2>How does CIDR work?</h2>
<p>CIDR is based on variable-length subnet masking (VLSM). This allows it to define prefixes of arbitrary lengths making it much more efficient than the old system. CIDR IP addresses are composed of two sets of numbers. The network address is written as a prefix, like you would see a normal IP address (e.g. 192.255.255.255). The second part is the suffix which indicates how many bits are in the entire address (e.g. /12). Putting it together, a CIDR IP address would look like the following:</p>
<pre class=" language-none"><code class=" language-none">192.255.255.255/12</code></pre>
<p>The network prefix is also specified as part of the IP address. This varies depending upon the number of bits required. Therefore, taking the example above, we can say that the first 12 bits are the network part of the address while the last 20 bits are for host addresses.</p>






  





