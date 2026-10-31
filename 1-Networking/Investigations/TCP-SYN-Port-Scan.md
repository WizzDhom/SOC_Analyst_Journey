# Investigation Report: TCP SYN Port Scanning

## 1. Overview

This investigation examines a simulated network traffic scenario involving repeated TCP SYN packets sent from one host to multiple ports on another host.

**Investigation Type:** Network Traffic Analysis
**Tool:** Wireshark (conceptual packet analysis)
**Classification:** Suspicious Activity
**Data Source:** Simulated packet capture summary

## 2. Observed Evidence

The following activities were observed:

* Source IP: `192.168.1.20`
* Destination IP: `192.168.1.50`
* Multiple TCP SYN packets were sent to ports 21, 22, 23, 80 and 443.
* The packets were sent within approximately two seconds.
* The destination host returned a TCP RST packet.

## 3. Analysis

Repeated SYN packets targeting different ports on the same destination host are consistent with TCP SYN port scanning.

Port scanning may be used to identify accessible services and discover potential entry points on a system.

A TCP RST response indicates that a connection was reset. However, this alone does not establish the status of every scanned port.

## 4. Investigation Findings

The observed traffic pattern is suspicious and may indicate reconnaissance activity.

However, the available evidence does not establish whether the activity was malicious or an authorized security scan.

## 5. Recommended Actions

1. Identify the source device and verify its ownership.
2. Determine whether network scanning was authorized.
3. Examine additional packet responses and traffic patterns.
4. Correlate findings with available firewall and endpoint logs.
5. Document findings and escalate if unauthorized activity is confirmed.

## 6. Conclusion

The observed network traffic is consistent with possible TCP SYN port scanning.

Further investigation is required before classifying the activity as a confirmed security incident.

---

**Learning Outcome:** Practised identifying suspicious TCP traffic, interpreting packet flags, classifying network activity and documenting investigation findings.
