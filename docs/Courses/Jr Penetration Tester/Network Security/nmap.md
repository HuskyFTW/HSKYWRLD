# Nmap Host Discovery Commands

You have learned how ARP, ICMP, TCP, and UDP can detect live hosts by completing this room. Any response from a host is an indication that it is online. Below is a quick summary of the command-line options for Nmap that we have covered.

## Scan Types and Example Commands

| Scan Type            | Example Command                           |
| -------------------- | ----------------------------------------- |
| ARP Scan             | `sudo nmap -PR -sn MACHINE_IP/24`         |
| ICMP Echo Scan       | `sudo nmap -PE -sn MACHINE_IP/24`         |
| ICMP Timestamp Scan  | `sudo nmap -PP -sn MACHINE_IP/24`         |
| ICMP Address Mask Scan| `sudo nmap -PM -sn MACHINE_IP/24`         |
| TCP SYN Ping Scan    | `sudo nmap -PS22,80,443 -sn MACHINE_IP/30`|
| TCP ACK Ping Scan    | `sudo nmap -PA22,80,443 -sn MACHINE_IP/30`|
| UDP Ping Scan        | `sudo nmap -PU53,161,162 -sn MACHINE_IP/30`|

Remember to add `-sn` if you are only interested in host discovery without port-scanning. Omitting `-sn` will let Nmap default to port-scanning the live hosts.

## Nmap Options

| Option | Purpose                         |
| ------ | ------------------------------- |
| -n     | No DNS lookup                   |
| -R     | Reverse-DNS lookup for all hosts|
| -sn    | Host discovery only             |

Ensure you have taken note of all the Nmap options explained in this room. To continue learning about Nmap, please join the room Nmap Basic Port Scans, which introduces the basic types of port scans.



# Nmap Scans and Port Discovery Commands

## Host Discovery Scans

You have learned how ARP, ICMP, TCP, and UDP can detect live hosts. Now, let's explore three types of port scans to discover running TCP and UDP services on a target host.

### Port Scan Types and Example Commands

| Port Scan Type    | Example Command                  |
| ----------------- | -------------------------------- |
| TCP Connect Scan  | `nmap -sT MACHINE_IP`             |
| TCP SYN Scan      | `sudo nmap -sS MACHINE_IP`        |
| UDP Scan          | `sudo nmap -sU MACHINE_IP`        |

These scan types should get you started in discovering running TCP and UDP services on a target host.

### Nmap Port Scan Options

| Option             | Purpose                                  |
| ------------------ | ---------------------------------------- |
| -p-                | Scan all ports                            |
| -p1-1023           | Scan ports 1 to 1023                      |
| -F                 | Scan the 100 most common ports            |
| -r                 | Scan ports in consecutive order           |
| -T<0-5>            | -T0 being the slowest and T5 the fastest  |
| --max-rate 50      | Set the rate to <= 50 packets/sec        |
| --min-rate 15      | Set the rate to >= 15 packets/sec        |
| --min-parallelism 100 | Set at least 100 probes in parallel     |

Ensure you understand these options for effective Nmap scanning. To continue learning about Nmap, consider joining the room "Nmap Basic Port Scans," which introduces the basic types of port scans.