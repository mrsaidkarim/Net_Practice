# Net_Practice


## TCP/IP Protocol
TCP/IP, which stands for Transmission Control Protocol/Internet Protocol, is a set of networking protocols that allows computers to communicate over networks like the internet. It provides the basic framework for transmitting data between devices and ensuring that data arrives accurately and in order.

## Components
TCP/IP operates on a layered model, with TCP and IP forming the two main layers:

- **Application Layer**: This layer includes protocols like HTTP, FTP, SMTP, and others that define how applications interact with the network.

- **Transport Layer**: TCP operates at this layer, providing reliable, connection-oriented communication between devices. UDP (User Datagram Protocol) is another protocol at this layer, offering a simpler, connectionless communication method suitable for applications that prioritize speed over reliability.

- **Internet Layer**: IP operates at this layer, handling addressing and routing of packets across networks.

- **Link Layer**: This layer deals with the physical connection between devices, including protocols for transmitting data over Ethernet, Wi-Fi, or other physical mediums.

## Initial Connection
When a device initially connects to a network, it typically doesn't have an IP address assigned yet. To communicate with the router or DHCP server to obtain an IP address, the device will use a special address called a link-local address.

A link-local address is an IP address that is automatically assigned to a device when it connects to a network and doesn't yet have an IP address. It allows the device to communicate with other devices on the same local network, including the router or DHCP server, without needing a pre-assigned IP address.

## Obtaining an IP Address
Once the device has a link-local address, it can then communicate with the router or DHCP server to request and obtain a proper IP address for internet communication. If there's no router involved, the device may directly communicate with the Internet Service Provider's infrastructure or the network it's connecting to.
