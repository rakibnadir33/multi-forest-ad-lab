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
