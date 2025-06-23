# cyber-security-task1

## Objective:
Perform a network port scan on the local network using Nmap and identify open ports.

## Tools Used:
- Nmap (via Zenmap GUI)

## Scan Command Used:
nmap -sS 192.168.1.0/24

## Scan Result Summary:
| IP Address   | Open Ports                  | Services         | Risk Level |
|-------------|----------------------------|-----------------|------------|
| 192.168.1.4 | 135/tcp, 445/tcp, 3306/tcp | msrpc, microsoft-ds, mysql | Medium |

## Possible Risks Identified:
- **135/tcp (msrpc)**: Can be used for RPC attacks if not properly secured.
- **445/tcp (microsoft-ds)**: Common ransomware target if SMB is exposed.
- **3306/tcp (mysql)**: MySQL database — risk of data exposure if unsecured.

## Files Included:
- `scan_result.txt` — Nmap scan output
- `README.md` — This documentation

## Conclusion:
The scan found 1 active device in the local network with 3 open ports. Proper security measures such as firewall, strong passwords, and updated software are needed to reduce risks.
