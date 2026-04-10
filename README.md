# Multi-Forest Active Directory Lab

![Active Directory](https://img.shields.io/badge/Active%20Directory-Attack%20Lab-blue?style=flat-square)
![Forests](https://img.shields.io/badge/Forests-2-darkred?style=flat-square)
![Domains](https://img.shields.io/badge/Domains-3-orange?style=flat-square)
![Machines](https://img.shields.io/badge/Machines-6-green?style=flat-square)

> ⚠️ Disclaimer: This lab was built in a fully isolated local environment for
> educational and research purposes only. All attack simulations were conducted
> against self-owned, air-gapped machines with no connection to any production
> or external network.

## Overview
A fully isolated enterprise-grade Active Directory lab built across four network
segments, simulating a real-world multi-forest enterprise environment with
cross-forest trust relationships and layered network pivoting requirements.
Every configuration reflects what you would find in a real enterprise environment
— not CTF shortcuts.

## Environment Structure

| Component | Details |
|---|---|
| Primary Forest | enterprise.dc |
| Child Domain | corp.enterprise.dc |
| Secondary Forest | manufacturing.local |
| Trust Type | Bidirectional Forest Trust |
| Total Machines | 6 |
| Network Segments | 4 isolated segments |

## Attack Path
To reach the manufacturing forest from the attacker machine, you must pivot
through each layer sequentially:

```
Attacker → External → DMZ → Corporate → Manufacturing
```

This mirrors a real enterprise breach — not a direct hop.

## What Was Simulated
- Network pivoting across four fully isolated segments
- Active Directory trust relationship enumeration and abuse
- Privilege escalation across domain boundaries
- Cross-forest compromise via bidirectional forest trust
- DCSync attacks for domain credential harvesting
- Kerberoasting and AS-REP roasting across domains

## Tools Used

| Tool | Purpose |
|---|---|
| BloodHound | AD attack path enumeration |
| Impacket | Remote execution and DCSync |
| Rubeus | Kerberos ticket manipulation |
| CrackMapExec | Lateral movement and enumeration |
| Mimikatz | Credential extraction |
| Proxychains | Network pivoting |

### Configuration Guide
![AD Multi-Forest Lab Configuration Guide](screenshots/02-configuration-guide.png)

📄 [Download Configuration Guide](config/AD-Multi-Forest-Configuration-Guide.pdf)

## Screenshots

### Lab Overview
![Cover](screenshots/01-cover.png)

### Configuration Guide
![AD Multi-Forest Lab Configuration Guide](screenshots/02-configuration-guide.png)

### Six Machines Across Segments
![6 machines](screenshots/03-six-machines.png)

### Three Domain Structure
![3 domains](screenshots/04-three-domains.png)

### Two Forest Architecture
![2 forests](screenshots/05-two-forests.png)

### Bidirectional Trust Configuration
![Bidirectional Trust](screenshots/06-bidirectional-trust.png)

## Author
**Rakib Mahmud Nadir**  
Junior Penetration Tester | Active Directory Security  
[Portfolio](https://rakibnadir33.github.io/rakibnadir.github.io/) · [LinkedIn](https://linkedin.com/in/rakib-nadir)
