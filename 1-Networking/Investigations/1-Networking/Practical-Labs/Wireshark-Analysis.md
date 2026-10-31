# Wireshark Practical Labs

## Overview

Wireshark was used to examine network traffic and understand how communication occurs between devices.

## Lab 1: DNS Traffic Analysis

**Objective:** Identify DNS queries and responses.

### Activities

* Captured network traffic using Wireshark.
* Applied the `dns` display filter.
* Identified DNS queries and corresponding responses.
* Examined source and destination IP addresses.
* Observed DNS response information.

### Key Learning

DNS translates domain names into IP addresses. Examining DNS traffic helps analysts understand domain lookup activity and investigate potentially suspicious DNS behaviour.

## Lab 2: TCP Three-Way Handshake

**Objective:** Understand how TCP connections are established.

### Activities

* Examined TCP packets in Wireshark.
* Identified SYN, SYN-ACK and ACK packets.
* Observed the sequence used to establish a TCP connection.

### Key Learning

The TCP three-way handshake establishes a connection between two devices before normal data transmission.

## Useful Wireshark Filters

| Filter                 | Purpose              |
| ---------------------- | -------------------- |
| `dns`                  | Display DNS traffic  |
| `tcp`                  | Display TCP traffic  |
| `tcp.flags.syn == 1`   | Identify SYN packets |
| `tcp.flags.ack == 1`   | Identify ACK packets |
| `tcp.flags.fin == 1`   | Identify FIN packets |
| `tcp.flags.reset == 1` | Identify RST packets |

## Conclusion

These exercises introduced practical packet analysis and demonstrated how Wireshark can support basic network troubleshooting and SOC investigations.
