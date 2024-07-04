# Net_Practice

## Network
A network consists of two or more computers that are linked in order to share resources (such as printers and CDs), exchange files, or allow electronic communications. The computers on a network may be linked through cables, telephone lines, radio waves, satellites, or infrared light beams.

## Network Types
- Personal Area Network (PAN) : is the most basic type of computer network. This network is restrained to a single person, that is, communication between the computer devices is centered only on an individual’s workspace. PAN offers a network range of 1 to 100 meters from person to device providing communication. Its transmission speed is very high with very easy maintenance and very low cost. This uses Bluetooth, IrDA, and Zigbee as technology. Examples of PAN are USB, computer, phone, tablet, printer, PDA, etc.
- Local Area Networks (LAN): LANs are networks that connect devices within a limited geographic area, such as a home, office, or campus. They typically use Ethernet or Wi-Fi technology and are often used for sharing resources such as files, printers, and internet access.
- Campus Area Network (CAN): CAN is bigger than a LAN but smaller than a MAN. This is a type of computer network that is usually used in places like a school or colleges. This network covers a limited geographical area that is, it spreads across several buildings within the campus. CAN mainly use Ethernet technology with a range from 1km to 5km. Its transmission speed is very high with a moderate maintenance cost and moderate cost. Examples of CAN are networks that cover schools, colleges, buildings, etc.
- Metropolitan Area Network (MAN) : A MAN is larger than a LAN but smaller than a WAN. This is the type of computer network that connects computers over a geographical distance through a shared communication path over a city, town, or metropolitan area. This network mainly uses FDDI, CDDI, and ATM as the technology with a range from 5km to 50km. Its transmission speed is average. It is difficult to maintain and it comes with a high cost. Examples of MAN are networking in towns, cities, a single large city, a large area within multiple buildings, etc.
- Wide Area Networks (WAN): WANs connect devices over a wide geographic area, often spanning multiple cities or countries. Examples include the internet, private leased lines, and virtual private networks (VPNs).

### Wireless Networking:
Wireless technologies enable communication between devices without the need for physical cables. Common wireless standards include Wi-Fi (802.11), Bluetooth, and cellular networks (e.g., 3G, 4G, 5G).

## IP Address
IP addressing is a logical means of assigning addresses to devices on a network. Each device connected to the internet requires a unique IP address.
An IP address has two parts; one part identifies the host such as a computer or other device, and the other part identifies the network it belongs to. TCP/IP uses a subnet mask to separate them.

## Initial Connection
When a device initially connects to a network, it typically doesn't have an IP address assigned yet. To communicate with the router or DHCP server to obtain an IP address, the device will use a special address called a link-local address.

A link-local address is an IP address that is automatically assigned to a device when it connects to a network and doesn't yet have an IP address. It allows the device to communicate with other devices on the same local network, including the router or DHCP server, without needing a pre-assigned IP address.

## Obtaining an IP Address
Once the device has a link-local address, it can then communicate with the router or DHCP server to request and obtain a proper IP address for internet communication. If there's no router involved, the device may directly communicate with the Internet Service Provider's infrastructure or the network it's connecting to.

## TCP/IP Protocol
TCP/IP, which stands for Transmission Control Protocol/Internet Protocol, is a set of networking protocols that allows computers to communicate over networks like the internet. It provides the basic framework for transmitting data between devices and ensuring that data arrives accurately and in order.

## Components
TCP/IP operates on a layered model, with TCP and IP forming the two main layers:

- **Application Layer**: This layer includes protocols like HTTP, FTP, SMTP, and others that define how applications interact with the network.

- **Transport Layer**: TCP operates at this layer, providing reliable, connection-oriented communication between devices. UDP (User Datagram Protocol) is another protocol at this layer, offering a simpler, connectionless communication method suitable for applications that prioritize speed over reliability.

- **Internet Layer**: IP operates at this layer, handling addressing and routing of packets across networks.

- **Link Layer**: This layer deals with the physical connection between devices, including protocols for transmitting data over Ethernet, Wi-Fi, or other physical mediums.


## Subnetting
When a bigger network is divided into smaller networks, to maintain security, then that is known as Subnetting. So, maintenance is easier for smaller networks. For example, if we consider a class A address, the possible number of hosts is 224 for each network, it is obvious that it is difficult to maintain such a huge number of hosts, but it would be quite easier to maintain if we divide the network into small parts.

### Steps in Subnetting
1. Determine the Number of Subnets Needed:
- Identify the number of subnets required and the number of hosts per subnet.

2. Calculate the Subnet Mask:
- Determine the subnet mask that will provide the necessary number of subnets and hosts.
- Subnet masks can be calculated by borrowing bits from the host portion of the address to create additional network bits.

3. Divide the Network:
- Using the new subnet mask, divide the original network into the required number of subnets.

4. Assign IP Ranges:
- Each subnet will have a range of IP addresses. The first address in each range is the subnet address, and the last address is the broadcast address. The addresses in between are available for hosts.

#### *Example*:
Let's say you have a network 192.168.1.0/24 and you need to create 4 subnets.

1. Determine the Number of Subnets Needed:
- 4 subnets require 2 additional bits (since 2^2 = 4).

2. Calculate the Subnet Mask:
- Original subnet mask: 255.255.255.0 (/24).
- New subnet mask: 255.255.255.192 (/26).

3. Divide the Network:
- 192.168.1.0/26
- 192.168.1.64/26
- 192.168.1.128/26
- 192.168.1.192/26

4. Assign IP Ranges:
- Subnet 1: 192.168.1.0 - 192.168.1.63 (subnet address: 192.168.1.0, broadcast address: 192.168.1.63)
- Subnet 2: 192.168.1.64 - 192.168.1.127 (subnet address: 192.168.1.64, broadcast address: 192.168.1.127)
- Subnet 3: 192.168.1.128 - 192.168.1.191 (subnet address: 192.168.1.128, broadcast address: 192.168.1.191)
- Subnet 4: 192.168.1.192 - 192.168.1.255 (subnet address: 192.168.1.192, broadcast address: 192.168.1.255)
