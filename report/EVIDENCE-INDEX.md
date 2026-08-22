# NovaShyld Task 3 — Evidence Index

## Target

- Target: Metasploitable 2
- IP: 192.168.19.129
- Assessment Interface: eth1

## Nmap Evidence

| ID | File | Purpose |
|---|---|---|
| NMAP-01 | `nmap/10-target-host-discovery.txt` | Target host discovery |
| NMAP-02 | `nmap/11-target-full-tcp.txt` | Full TCP port enumeration |
| NMAP-03 | `nmap/12-target-service-version.txt` | TCP service/version enumeration |
| NMAP-04 | `nmap/13-target-os-detection.txt` | OS fingerprinting |
| NMAP-05 | `nmap/14-target-udp-top20.txt` | UDP enumeration |
| NMAP-06 | `nmap/15-udp-service-validation.txt` | UDP service validation |

## Supporting Enumeration Evidence

| ID | File | Purpose |
|---|---|---|
| NMAP-07 | `nmap/02-tcp-basic.txt` | Initial TCP scan |
| NMAP-08 | `nmap/03-vmware-network-device.txt` | Network-device observation |
| NMAP-09 | `nmap/04-udp-top20.txt` | UDP reconnaissance |
| NMAP-10 | `nmap/05-mysql-version.txt` | MySQL service validation |
| NMAP-11 | `nmap/06-os-detection.txt` | OS detection |
| NMAP-12 | `nmap/07-full-tcp.txt` | Full TCP scan |
| NMAP-13 | `nmap/08-service-version-all.txt` | Service/version validation |
| NMAP-14 | `nmap/09-closed-port-check.txt` | Closed/filtered port validation |

## OSINT Evidence

| ID | File | Purpose |
|---|---|---|
| OSINT-01 | `osint/OSINT-NOTES.md` | Passive OSINT methodology and results |

## Wireshark Evidence

| ID | File | Purpose |
|---|---|---|
| WIRESHARK-01 | `wireshark/target-recon.pcapng` | Packet-level reconnaissance capture |

## Reports

| ID | File | Purpose |
|---|---|---|
| REPORT-01 | `report/Network-Service-Enumeration.md` | Network/service enumeration sheet |
| REPORT-02 | `report/Target-Profile.md` | Target profile |
| REPORT-03 | `report/EVIDENCE-INDEX.md` | Evidence mapping |

## Evidence Integrity

All technical findings are based on commands actually executed during the
assessment. No unsupported exploitation result is claimed for Task 3.
