# NovaShyld Task 3 — Network & Service Enumeration

## Target

| Field | Value |
|---|---|
| Target | Metasploitable 2 |
| IP Address | 192.168.19.129 |
| MAC Address | 00:0C:29:FA:DD:34 |
| Network | 192.168.19.0/24 |
| Kali Interface | eth1 |
| Kali IP | 192.168.19.128 |

## Operating System

Nmap OS detection identified the target as a general-purpose Linux system running
Linux 2.6.x. Nmap estimated the kernel range as Linux 2.6.9–2.6.33.

## TCP Services

| Port | Protocol | Service | Version |
|---:|---|---|---|
| 21 | TCP | FTP | vsftpd 2.3.4 |
| 22 | TCP | SSH | OpenSSH 4.7p1 Debian 8ubuntu1 |
| 23 | TCP | Telnet | Linux telnetd |
| 25 | TCP | SMTP | Postfix smtpd |
| 53 | TCP | DNS | ISC BIND 9.4.2 |
| 80 | TCP | HTTP | Apache httpd 2.2.8 |
| 111 | TCP | RPCbind | 2 |
| 139 | TCP | NetBIOS | Samba smbd 3.X–4.X |
| 445 | TCP | SMB | Samba smbd 3.X–4.X |
| 512 | TCP | rexec | netkit-rexecd |
| 513 | TCP | login | Netkit |
| 514 | TCP | shell | Netkit rshd |
| 1099 | TCP | Java RMI | GNU Classpath grmiregistry |
| 1524 | TCP | bindshell | Metasploitable root shell |
| 2049 | TCP | NFS | RPC #100003 |
| 2121 | TCP | FTP | ProFTPD 1.3.1 |
| 3306 | TCP | MySQL | MySQL 5.0.51a |
| 3632 | TCP | distccd | distccd v1 |
| 5432 | TCP | PostgreSQL | PostgreSQL 8.3.x |
| 5900 | TCP | VNC | VNC protocol 3.3 |
| 6000 | TCP | X11 | Access denied |
| 6667 | TCP | IRC | UnrealIRCd |
| 6697 | TCP | IRC | UnrealIRCd |
| 8009 | TCP | AJP13 | Apache Jserv |
| 8180 | TCP | HTTP | Apache Tomcat/Coyote |
| 8787 | TCP | DRb | Ruby DRb RMI |
| 33398 | TCP | mountd | RPC #100005 |
| 41892 | TCP | Java RMI | GNU Classpath grmiregistry |
| 51180 | TCP | nlockmgr | RPC #100021 |
| 55243 | TCP | status | RPC #100024 |

## UDP Services

| Port | Protocol | State | Service | Version |
|---:|---|---|---|---|
| 53 | UDP | Open | DNS | ISC BIND 9.4.2 |
| 137 | UDP | Open | NetBIOS Name Service | WORKGROUP |
| 68 | UDP | Open\|filtered | DHCP client | Not confirmed |
| 69 | UDP | Open\|filtered | TFTP | Not confirmed |
| 138 | UDP | Open\|filtered | NetBIOS Datagram | Not confirmed |

Additional tested UDP ports 162, 500, 1434 and 49152 were subsequently identified as closed.

## Hostnames / Identifiers

- metasploitable.localdomain
- irc.Metasploitable.LAN
- METASPLOITABLE
- WORKGROUP

## Reconnaissance Evidence

Evidence was collected using:

- Nmap host discovery
- Full TCP SYN scanning
- TCP service/version detection
- OS detection
- UDP top-port enumeration
- Targeted UDP service validation
- Wireshark packet capture

## Accuracy Notes

`open|filtered` UDP results are not treated as confirmed open services.

The UDP service detection output contained a generic Windows service fingerprint,
but the dedicated OS detection identified the target as Linux 2.6.x. The dedicated
OS fingerprint and corroborating service banners are therefore kept as separate
evidence rather than treating the UDP fingerprint as an exact OS identification.
