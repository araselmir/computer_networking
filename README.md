# A. Layers of OSI Model
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
<p>This is the layer responsible for opening and closing communication between the two devices. The time between when the communication is opened and closed is known as the session. The session layer ensures that the session stays open long enough to transfer all the data being exchanged, and then promptly closes the session in order to avoid wasting resources.</p>
<p>The session layer also synchronizes data transfer with checkpoints. For example, if a 100 megabyte file is being transferred, the session layer could set a checkpoint every 5 megabytes. In the case of a disconnect or a crash after 52 megabytes have been transferred, the session could be resumed from the last checkpoint, meaning only 50 more megabytes of data need to be transferred. Without the checkpoints, the entire transfer would have to begin again from scratch.</p>
  
  
  ![Screenshot from 2020-09-10 16-33-54](https://user-images.githubusercontent.com/62602944/92719002-61c8be80-f384-11ea-8702-2a7e425fbe5f.png)
  
  <h3>4. The Transport Layer</h3>
  <p>Layer 4 is responsible for end-to-end communication between the two devices. This includes taking data from the session layer and breaking it up into chunks called segments before sending it to layer 3. The transport layer on the receiving device is responsible for reassembling the segments into data the session layer can consume.</p>
  <p>The transport layer is also responsible for flow control and error control. Flow control determines an optimal speed of transmission to ensure that a sender with a fast connection doesn’t overwhelm a receiver with a slow connection. The transport layer performs error control on the receiving end by ensuring that the data received is complete, and requesting a retransmission if it isn’t.</p>
  
  ![Screenshot from 2020-09-10 16-33-57](https://user-images.githubusercontent.com/62602944/92719020-67260900-f384-11ea-8bbd-83984b6e5d02.png)

<h3>3. The Network Layer</h3>
<p>The network layer is responsible for facilitating data transfer between two different networks. If the two devices communicating are on the same network, then the network layer is unnecessary. The network layer breaks up segments from the transport layer into smaller units, called packets, on the sender’s device, and reassembling these packets on the receiving device. The network layer also finds the best physical path for the data to reach its destination; this is known as routing.</p>

![Screenshot from 2020-09-10 16-34-00](https://user-images.githubusercontent.com/62602944/92719036-6db48080-f384-11ea-9fed-34d5361a7a9a.png)

<h3>2. The Data Link Layer</p>
<p>The data link layer is very similar to the network layer, except the data link layer facilitates data transfer between two devices on the SAME network. The data link layer takes packets from the network layer and breaks them into smaller pieces called frames. Like the network layer, the data link layer is also responsible for flow control and error control in intra-network communication (The transport layer only does flow control and error control for inter-network communications).</p>

![Screenshot from 2020-09-10 16-34-02](https://user-images.githubusercontent.com/62602944/92719060-72793480-f384-11ea-9232-7803e88a3e7b.png)

<h3>1. The Physical Layer</h3>
<p>This layer includes the physical equipment involved in the data transfer, such as the cables and switches. This is also the layer where the data gets converted into a bit stream, which is a string of 1s and 0s. The physical layer of both devices must also agree on a signal convention so that the 1s can be distinguished from the 0s on both devices.</p>

![Screenshot from 2020-09-10 16-34-06](https://user-images.githubusercontent.com/62602944/92719074-75742500-f384-11ea-81d8-95ff38a12fd9.png)


