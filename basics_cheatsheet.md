**OSI Model:** Divides the internet as we know today in 7 layers where the 7th layer, the application layer, is built on top of all the other layers. 
![[Pasted image 20241017160236.png]]

**Encapsulation of data:** When it is said that the top layer is built on top of the bottom layers, it means encapsulation. Basically every layer is built by a header and a payload/SDU. Both parts together is called PDU. The catch is that the payload of the lower layer is the PDU of the higher layer so we get something similar to a Russian doll.  
PDU = Protocol Data Unit
SDU = Service Data Unit
![[Pasted image 20241017161041.png]]


![[Pasted image 20241017161319.png]]
Every new doll that encapsulates the smaller ones are a new header of a lower layer.

## Layer 2

**MAC Addresses: **
![[Pasted image 20241017161742.png]]
- 48 bits = 6 bytes in length;
- OUI = Organizationally Unique Identifier. These are given to the big companies that produces internet capable devices;
- Device ID is the identification of a device manufactured by a company.

**Ethernet Frame:**
![[Pasted image 20241017162307.png]]
The first 12 bytes correspond to the Ethernet Header
- Destination Address = MAC address of the destination (next hop);
- Source Address = MAC address of the sender;
- Ethertype = type of layer 3 protocol that comes next (usually ipv4 or ipv6). 
![[Pasted image 20241017162842.png]]

**Layer 2 Traffic:**
The device that manages traffic in layer 2 is called a switch. 


## Layer 3 - The Internet Protocol
ipv6 Header:![[Pasted image 20241017164636.png]]
- Version : 6
- Traffic Class and Flow Label are meant for QOS (Quality Of Service) ends.
- Payload Length: size of payload after the header;
- Next Header: specifies which protocol header comes after. Usually UDP or TCP but also fragment headers;
- Hop Limit: specifies how many hops the packet has left before it is dropped by a router. Standard starting amount are 64 hops;
- Source Address = Sender's ipv6 address
- Destination Address = Final target address

**ipv6 addresses:**
![[Pasted image 20241017172750.png]]

