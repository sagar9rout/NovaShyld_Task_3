# NovaShyld Task 3 — Target Profile

## 1. Target Overview

The assessed system is a Metasploitable 2 virtual machine located inside the
CyberLab isolated network.

**Target IP:** 192.168.19.129

**MAC:** 00:0C:29:FA:DD:34

**Network:** 192.168.19.0/24

**Assessment interface:** eth1

## 2. Network Position

The Kali assessment system used:

- eth1: 192.168.19.128/24
- Target: 192.168.19.129/24

The target was one network hop from Kali.

## 3. Operating System

Nmap OS detection identified:

- General-purpose Linux
- Linux 2.6.x
- Estimated kernel range: 2.6.9–2.6.33

## 4. Network Exposure

The target exposed a large TCP attack surface, with 31 TCP ports identified as
open during full-port enumeration.

Important services included:

- FTP
- SSH
- Telnet
- SMTP
- DNS
- HTTP
- SMB/NetBIOS
- RPC
- NFS
- MySQL
- PostgreSQL
- VNC
- IRC
- AJP13
- Apache Tomcat
- Java RMI
- Ruby DRb

Confirmed UDP services included:

- UDP/53 — ISC BIND 9.4.2
- UDP/137 — NetBIOS Name Service

Several UDP ports returned open|filtered and were not treated as confirmed
services.

## 5. Hostnames and Service Identifiers

Observed identifiers included:

- metasploitable.localdomain
- irc.Metasploitable.LAN
- METASPLOITABLE
- WORKGROUP

## 6. Passive OSINT

The assignment's passive reconnaissance requirement was addressed using the OSINT
Framework methodology.

Because the target is a private RFC1918 address inside the CyberLab environment,
public Internet intelligence for 192.168.19.129 is inherently limited.

Lab-derived identifiers were documented separately from public Internet findings.

## 7. Wireshark Analysis

A packet capture was performed on eth1 using:

    ip.addr == 192.168.19.129

The capture demonstrated:

- ICMP Echo Request packets from Kali to the target
- ICMP Echo Reply packets from the target
- TCP SYN packets generated during service reconnaissance
- TCP SYN/ACK responses from reachable services
- TCP reset traffic associated with connection termination

The capture provides packet-level evidence supporting the active reconnaissance
activity.

## 8. Security Assessment Observation

The target presents a broad network attack surface due to the large number of
exposed services and legacy software versions.

This Task 3 assessment focuses on reconnaissance and enumeration. Exploitation
activities were intentionally not repeated because they were outside the scope
of this assignment and were addressed during the previous Metasploitable 2
assessment.

## 9. Conclusion

The reconnaissance phase successfully established the target's network identity,
operating-system fingerprint, exposed TCP/UDP services, service versions,
hostnames, and packet-level reconnaissance behavior.

The resulting evidence provides the foundation for the required NovaShyld Task 3
Network & Service Enumeration Sheet and Target Profile documentation.
