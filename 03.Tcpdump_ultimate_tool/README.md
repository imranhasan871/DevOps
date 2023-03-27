# Ip Header Format and Tcpdump Command Line Tool with Scenario Examples

## What is IP Header Format?

The IP header is the first part of the IP packet. It contains the source and destination IP addresses, the protocol, and other information. The IP header is 20 bytes long. The IP header is the first part of the IP packet. It contains the source and destination IP addresses, the protocol, and other information. The IP header is 20 bytes long.

<!-- Insert here an image markdown -->
![image info](./images/1.png)

<!-- Write IP Header Fields indetail -->

# 🌍 IP Header Fields

## 📥 Source IP Address and 📤 Destination IP Address

The source IP address field in the IP header identifies the sender of the packet, while the destination IP address field identifies the intended recipient of the packet. Just like sending a letter, you need to put your address (source IP) and the address of the recipient (destination IP) on the envelope to ensure it gets delivered to the right place.

## 📦 Type of Service (TOS) and 🚥 Differentiated Services Code Point (DSCP)

The TOS field is used to specify the priority and quality of service for the packet. In modern IP networks, the TOS field is usually replaced by the DSCP field, which allows for more granular QoS control.

## 🕰️ Identification

The identification field is used to uniquely identify each IP packet. This field is used in fragmentation and reassembly of IP packets.

## 🎨 Flags

The flags field contains three bits used to control fragmentation of IP packets. The first bit is the "reserved" bit and is always set to zero. The second bit is the "don't fragment" (DF) bit, which, when set, indicates that the packet should not be fragmented. The third bit is the "more fragments" (MF) bit, which, when set, indicates that the packet is part of a fragmented packet and that more fragments are expected.

## 🧱 Fragment Offset

The fragment offset field is used to indicate the offset of the current fragment relative to the start of the original IP packet. This field is used in fragmentation and reassembly of IP packets.

## 🔒 Time to Live (TTL)

The TTL field is used to limit the lifetime of an IP packet. The value in this field is decremented by one at each router hop, and if it reaches zero, the packet is discarded.

## 🧭 Protocol

The protocol field is used to identify the transport protocol that is carried in the payload of the IP packet. For example, TCP, UDP, ICMP, etc.

## 📐 Header Checksum

The header checksum field is used to ensure the integrity of the IP header. It is computed over the entire IP header, and any changes to the header will result in a different checksum value.

## 📦 Options

The options field is used to carry additional information about the IP packet. This field is optional and is not often used in practice.

## 📈 Total Length

The total length field specifies the length of the entire IP packet, including the IP header and the payload. The maximum value for this field is 65,535 bytes.

## 🧬 Version

The version field specifies the version of the IP protocol. Currently, the most widely used version is IPv4 (version 4), but there is also a newer version called IPv6 (version 6).

## 🚦 Header Length

The header length field specifies the length of the IP header in 32-bit words. This field is used to determine the start of the payload in the IP packet.

## 🔑 Options Padding

The options padding field is used to ensure that the IP header is aligned on a 32-bit boundary. This field is only used if the options field is present.

# What is tcpdump?

Tcpdump is a command-line network sniffer that can be used to capture and display network traffic. It is a powerful tool that can be used to troubleshoot network problems, monitor network traffic, and perform network forensics. It is available on most Unix-like operating systems, including Linux, macOS, and FreeBSD. It is also available on Windows, but it is not installed by default.
