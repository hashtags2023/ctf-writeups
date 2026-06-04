# What is Networking? — TryHackMe

**Date:** 2026-06-04
**Platform:** TryHackMe
**Path:** Pre-Security → Network Fundamentals
**Category:** Networking
**Difficulty:** Easy
**Room:** [What is Networking?](https://tryhackme.com/room/whatisnetworking)
**Status:** ✅ Complete

---

## Task 1 — What is Networking?

Networks are simply things connected — this applies everywhere, not just in computing. Examples include public transportation systems, power grids, postal systems, and social circles.

In computing, a network can be formed by anywhere from 2 devices to billions — laptops, phones, security cameras, traffic lights, and more. Because networks are so embedded in modern life, networking is an essential concept in cybersecurity.

### Answer

| Question                                                      | Answer    |
| ------------------------------------------------------------- | --------- |
| What is the key term for devices that are connected together? | `Network` |

---

## Task 2 — What is the Internet?

The Internet is one giant network made up of many smaller networks. It began as the **ARPANET** project in the late 1960s, funded by the United States Defence Department — the first documented network in action.

In 1989, **Tim Berners-Lee** invented the World Wide Web (WWW), which transformed the Internet into a repository for storing and sharing information as we know it today.

Networks are one of two types:

- **Private network** — devices communicating internally
- **Public network** — the Internet connecting private networks together

### Answer

| Question                         | Answer            |
| -------------------------------- | ----------------- |
| Who invented the World Wide Web? | `Tim Berners-Lee` |

---

## Task 3 — Identifying Devices on a Network

Devices on a network need two means of identification:

### IP Addresses

An **IP address (Internet Protocol)** identifies a host on a network. It is made up of four **octets** (e.g. `192.168.1.77`).

- **Private IP** — identifies a device within a local network
- **Public IP** — identifies a device on the Internet (assigned by your ISP)

**IPv4** uses a 2^32 numbering system (~4.29 billion addresses) — increasingly insufficient as more devices connect.

**IPv6** was introduced to solve this, supporting 2^128 addresses (~340 trillion+) and offering more efficient routing.

### MAC Addresses

A **MAC (Media Access Control) address** is a unique hardware identifier assigned to a device's network interface at the factory. It is a 12-character hexadecimal number split by colons (e.g. `a4:c3:f0:85:ac:2d`).

- First 6 characters = manufacturer identifier
- Last 6 characters = unique device number

**MAC Spoofing** is when a device fakes another device's MAC address. This can bypass poorly implemented security — for example, a firewall configured to trust a specific MAC address could be fooled by a spoofed device.

### Practical — Hotel Wi-Fi MAC Spoofing Lab

The interactive lab simulates a hotel Wi-Fi network. Bob's packets were being blocked because he hadn't paid for access, while Alice's packets passed through freely. By spoofing Bob's MAC address to match Alice's, his traffic was allowed through.

**Flag:** `THM{YOU_GOT_ON_TRYHACKME}`

### Answers

| Question                                                 | Answer                      |
| -------------------------------------------------------- | --------------------------- |
| What does the term "IP" stand for?                       | `Internet Protocol`         |
| What is each section of an IP address called?            | `Octet`                     |
| How many sections (in digits) does an IPv4 address have? | `4`                         |
| What does the term "MAC" stand for?                      | `Media Access Control`      |
| What is the flag from the interactive lab?               | `THM{YOU_GOT_ON_TRYHACKME}` |

---

## Task 4 — Ping (ICMP)

**Ping** is a fundamental network tool that uses **ICMP (Internet Control Message Protocol)** packets to test the performance and reliability of a connection between devices.

It works by sending an **ICMP echo** packet to a target and measuring the time it takes to receive an **ICMP echo reply**.

**Syntax:**

```bash
ping <IP address or URL>
```

**Example:**

```bash
ping 192.168.1.254
```

Pinging `8.8.8.8` (Google's public DNS server) in the interactive lab returned the flag.

**Flag:** `THM{I_PINGED_THE_SERVER}`

### Answers

| Question                                    | Answer                     |
| ------------------------------------------- | -------------------------- |
| What protocol does ping use?                | `ICMP`                     |
| What is the syntax to ping 10.10.10.10?     | `ping 10.10.10.10`         |
| What flag do you get when you ping 8.8.8.8? | `THM{I_PINGED_THE_SERVER}` |

---

## Task 5 — Continue Your Learning: Intro to LAN

Next room: **[Intro to LAN](https://tryhackme.com/room/introtolan)**

---

## Key Takeaways

1. A network is any group of connected devices — from 2 to billions
2. The Internet is a public network made up of many private networks
3. Devices are identified by **IP addresses** (logical, changeable) and **MAC addresses** (hardware, but spoofable)
4. IPv4 is running out of addresses — IPv6 solves this with a vastly larger address space
5. MAC spoofing is a real attack that can bypass security controls relying solely on MAC-based authentication
6. Ping uses ICMP to test connectivity and measure latency between devices

---

## Tools Used

- `ping` — ICMP connectivity testing
- TryHackMe interactive browser lab — MAC spoofing simulation

## References

- [TryHackMe — What is Networking?](https://tryhackme.com/room/whatisnetworking)
- [Cisco 2021 Connected Devices Estimate](https://www.cisco.com)
- [Tim Berners-Lee & the WWW](https://www.w3.org/People/Berners-Lee/)
