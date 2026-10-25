# Windows Network Troubleshooting & Diagnostics

## Project Overview

A practical IT Support and Network Troubleshooting project performed using Windows PowerShell. The project demonstrates network connectivity testing, IP configuration analysis, DNS troubleshooting, and route tracing.

## Project Objectives

- Analyze Windows IP configuration and network adapter settings.
- Verify local router and internet connectivity.
- Diagnose DNS resolution issues.
- Trace the network path to an external destination.
- Document troubleshooting findings and results.

## Tools & Technologies

- Windows PowerShell
- TCP/IP Networking
- IPv4 and IPv6
- DNS (Domain Name System)
- ICMP / Ping
- Traceroute

## Commands Used

```powershell
ipconfig /all
ping 192.168.1.1
ping 8.8.8.8
ping google.com
nslookup google.com
nslookup google.com 8.8.8.8
tracert google.com
```

## Test Results

| Test | Result | Status |
|---|---|---|
| IP Configuration | Valid IPv4 address, gateway and DNS configuration observed | Completed |
| Router Ping | 2 ms average, 0% packet loss | Passed |
| Internet Ping | 5 ms average, 0% packet loss | Passed |
| Google Ping | 7 ms average, 0% packet loss | Passed |
| Default DNS Lookup | DNS request timed out | Investigation Required |
| Google DNS Lookup (8.8.8.8) | Domain successfully resolved | Passed |
| Traceroute | Destination reached at hop 21 | Passed |

## DNS Troubleshooting Findings

During testing, the default DNS server (`fe80::1`) did not respond to the `nslookup` request.

A second lookup was performed using Google Public DNS (`8.8.8.8`), which successfully resolved `google.com` into IPv4 and IPv6 addresses.

This indicates that external DNS resolution was working during the test, while the default DNS lookup experienced a timeout. Further testing would be required to confirm the exact cause.

## Traceroute Analysis

The traceroute to `google.com` completed successfully using IPv6.

Some intermediate hops did not respond to traceroute probes. However, the final destination was reached at hop 21.

## Key Skills Demonstrated

- Windows Network Diagnostics
- TCP/IP Troubleshooting
- DNS Resolution Testing
- Network Connectivity Analysis
- PowerShell Commands
- Technical Documentation
- IT Support Problem Investigation

## Project Documentation

See the [Network Troubleshooting PDF Report](Windows_Network_Troubleshooting_Report.pdf) for detailed analysis and results.

## Conclusion

This project demonstrates practical troubleshooting of local network connectivity, internet access, DNS resolution, and network routing using Windows PowerShell.

**Project Type:** Technical Support / IT Help Desk / Network Troubleshooting

**Author:** Chetan Sharma
