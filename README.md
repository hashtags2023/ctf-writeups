# 🚩 CTF Writeups — Capture The Flag Solutions & Notes

> A collection of my CTF (Capture The Flag) challenge writeups. Each writeup documents my methodology, tools used, thought process, and key takeaways. Written to reinforce learning and help others in the community.

[![TryHackMe](https://img.shields.io/badge/TryHackMe-In%20Progress-red?style=flat)](https://tryhackme.com)
[![Platforms](https://img.shields.io/badge/Platforms-THM%20%7C%20HTB%20%7C%20PicoCTF-blue?style=flat)](#)
[![Focus](https://img.shields.io/badge/Focus-Blue%20%26%20Red%20Team-purple?style=flat)](#)

---

## 📋 Table of Contents

- [What is CTF?](#what-is-ctf)
- [How to Get Started](#how-to-get-started)
- [My Progress Tracker](#my-progress-tracker)
- [Writeups](#writeups)
- [Tools Reference](#tools-reference)
- [Resources](#resources)

---

## What is CTF?

A **Capture The Flag (CTF)** is a cybersecurity competition or challenge where you solve puzzles to find hidden "flags" — usually strings like `flag{s0m3_s3cr3t_t3xt}`. They're one of the best ways to build real, hands-on security skills.

### CTF Categories

| Category                      | What You Do                                                |
| ----------------------------- | ---------------------------------------------------------- |
| **Web**                       | Find vulnerabilities in websites (SQLi, XSS, IDOR, etc.)   |
| **Forensics**                 | Analyze files, memory dumps, packet captures               |
| **Cryptography**              | Break or decode ciphers and encryption                     |
| **Reverse Engineering**       | Analyze compiled binaries to understand what they do       |
| **Pwn / Binary Exploitation** | Exploit memory vulnerabilities (buffer overflow, etc.)     |
| **OSINT**                     | Find information using open-source intelligence techniques |
| **Steganography**             | Find data hidden inside images, audio, or other files      |
| **Miscellaneous**             | Anything that doesn't fit neatly elsewhere                 |

---

## How to Get Started

### Step 1 — Pick a Beginner-Friendly Platform

**Start here → [TryHackMe](https://tryhackme.com)** (most beginner-friendly, guided learning paths)

| Platform                                             | Difficulty              | Best For                                | Cost        |
| ---------------------------------------------------- | ----------------------- | --------------------------------------- | ----------- |
| [TryHackMe](https://tryhackme.com)                   | Beginner → Intermediate | Guided rooms, learning paths            | Free + Paid |
| [PicoCTF](https://picoctf.org)                       | Beginner                | Pure CTF challenges, great for learning | Free        |
| [Hack The Box](https://hackthebox.com)               | Intermediate → Advanced | Machines, realistic scenarios           | Free + Paid |
| [CTFtime.org](https://ctftime.org)                   | Varies                  | Live competitions, find upcoming CTFs   | Free        |
| [Blue Team Labs Online](https://blueteamlabs.online) | Beginner → Intermediate | Defensive/SOC-focused challenges        | Free + Paid |

### Step 2 — Recommended Learning Path (Do These in Order)

**Month 1 — TryHackMe Beginner Rooms**

1. [Complete Beginner Path](https://tryhackme.com/path/outline/beginner) — Linux basics, networking, web fundamentals
2. [Pre-Security Path](https://tryhackme.com/path/outline/presecurity) — How the internet, networks, and web apps work
3. [Introduction to Cybersecurity](https://tryhackme.com/path/outline/introtocyber) — Offensive vs defensive overview

**Month 2 — PicoCTF**

- Head to [picoctf.org](https://picoctf.org) and work through the **practice archive**
- Start with: General Skills → Forensics → Web → Cryptography
- Each challenge has a point value — lower = easier

**Month 3+ — Hack The Box & Live CTFs**

- Try "Starting Point" machines on HTB (guided)
- Watch [IppSec on YouTube](https://www.youtube.com/c/ippsec) for HTB walkthroughs
- Sign up on [CTFtime.org](https://ctftime.org) and participate in beginner-friendly team competitions

### Step 3 — Set Up Your Tools

```bash
# If using Kali Linux (recommended), most tools are pre-installed
# Key tools to know:
nmap            # Network/port scanning
gobuster        # Web directory brute-forcing
burpsuite       # Web proxy / intercept
john / hashcat  # Password cracking
binwalk         # Firmware/file analysis
steghide        # Steganography extraction
strings         # Extract readable strings from binaries
file            # Identify file types
xxd / hexdump   # Hex inspection
cyberchef       # Encoding/decoding (browser-based: gchq.github.io/CyberChef)
```

### Step 4 — Write Everything Down

Even if you needed hints or a walkthrough — **document it**. The writeup process forces you to truly understand what happened and builds your portfolio.

---

## My Progress Tracker

| #   | Platform  | Challenge / Room         | Category           | Difficulty | Date       | Status         |
| --- | --------- | ------------------------ | ------------------ | ---------- | ---------- | -------------- |
| 1   | TryHackMe | [Room Name]              | [Category]         | Easy       | [Date]     | ✅ Complete    |
| 2   | TryHackMe | Offensive Security Intro | Offensive Security | Easy       | 2026-05-27 | ✅ Complete    |
| 2   | TryHackMe | Careers in Cyber         | Learning           | Easy       | 2026-01-26 | ✅ Complete    |
| 2   | PicoCTF   | [Challenge Name]         | Forensics          | Easy       | [Date]     | ✅ Complete    |
| 3   | PicoCTF   | [Challenge Name]         | Web                | Medium     | [Date]     | 🔄 In Progress |

_(Update this table as you complete challenges)_

---

## Writeups

> Each writeup lives in its own folder. Template below.

### Index

| Challenge                                                          | Platform    | Category     | Difficulty | Flag |
| ------------------------------------------------------------------ | ----------- | ------------ | ---------- | ---- |
| [Example — Bandit Level 0](writeups/overthewire/bandit-level-0.md) | OverTheWire | Linux Basics | Easy       | ✅   |

---

## Writeup Template

> Copy this template when creating a new writeup.

---

````markdown
# [Challenge Name] — [Platform]

**Date:** YYYY-MM-DD  
**Platform:** TryHackMe / PicoCTF / HTB / etc.  
**Category:** Web / Forensics / Crypto / etc.  
**Difficulty:** Easy / Medium / Hard  
**Points:** XXX  
**Flag:** `flag{REDACTED}` _(or show it if the challenge is retired/public)_

---

## Challenge Description

> Paste the original challenge description here.

---

## Reconnaissance / Initial Thoughts

What did you notice first? What approach did you decide to take and why?

---

## Solution Walkthrough

### Step 1 — [What you did]

Explain your first step. Include commands you ran:

```bash
nmap -sV -sC 10.10.X.X
```
````

What did you find? What was interesting?

### Step 2 — [What you did next]

Continue documenting each meaningful step. Include:

- Commands / code used
- Screenshots or tool output (add images to `/writeups/[name]/assets/`)
- Why you made each decision

### Step 3 — Getting the Flag

Explain exactly how you captured the flag.

---

## Tools Used

- `nmap` — Port scanning
- `gobuster` — Directory enumeration
- [Add others]

---

## Key Takeaways

What did you learn? What would you do differently? What concept does this challenge demonstrate?

1. [Takeaway 1]
2. [Takeaway 2]
3. [Takeaway 3]

---

## References

- [Link to relevant documentation or resource]
- [CVE or vulnerability reference if applicable]

````

---

## Tools Reference

### Web Exploitation
```bash
# Directory/file brute-force
gobuster dir -u http://target.com -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

# Subdomain enumeration
gobuster dns -d target.com -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt

# SQL injection testing
sqlmap -u "http://target.com/page?id=1" --dbs

# Nikto web scan
nikto -h http://target.com
````

### Forensics & Steganography

```bash
# Identify file type
file suspicious_file

# Extract strings from binary
strings suspicious_file | less

# Check file for hidden data
binwalk suspicious_image.png

# Extract hidden data from image
steghide extract -sf image.jpg

# Analyze image metadata
exiftool image.jpg

# Hex dump
xxd file.bin | head -50
```

### Cryptography

```bash
# Identify hash type
hashid 5f4dcc3b5aa765d61d8327deb882cf99

# Crack hash with John
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt

# Crack hash with Hashcat
hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt

# Base64 decode
echo "aGVsbG8=" | base64 -d

# ROT13
echo "uryyb" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

### Network Analysis (Wireshark filters)

```
# HTTP traffic only
http

# Follow a TCP stream — right-click a packet → Follow → TCP Stream

# Find credentials in clear text
http.request.method == "POST"

# Filter by IP
ip.addr == 10.10.X.X

# DNS queries
dns
```

### Useful Online Tools

| Tool         | URL                              | Use                                |
| ------------ | -------------------------------- | ---------------------------------- |
| CyberChef    | https://gchq.github.io/CyberChef | Encoding, decoding, everything     |
| CrackStation | https://crackstation.net         | Hash lookup                        |
| dCode        | https://www.dcode.fr/en          | Cipher identifier + decoder        |
| Decode.fr    | https://www.decode.fr            | Many encodings                     |
| Shodan       | https://www.shodan.io            | OSINT / internet-connected devices |
| VirusTotal   | https://www.virustotal.com       | Malware analysis                   |

---

## Resources

### Learning

- [TryHackMe Learning Paths](https://tryhackme.com/paths) — Best structured beginner content
- [PicoCTF Archive](https://play.picoctf.org/practice) — Hundreds of free challenges
- [CTF101](https://ctf101.org) — Category-by-category CTF guide
- [IppSec YouTube](https://www.youtube.com/c/ippsec) — HTB machine walkthroughs
- [John Hammond YouTube](https://www.youtube.com/c/JohnHammond010) — CTF walkthroughs and security content
- [LiveOverflow YouTube](https://www.youtube.com/c/LiveOverflow) — Binary exploitation deep dives

### Find Live CTFs

- [CTFtime.org](https://ctftime.org) — Calendar of upcoming competitions worldwide
- Look for **beginner-friendly** tags, or team up with others on CTFtime's team finder

---

_hashtags2023 | B.S. Computer Science — CSU Sacramento | Cybersecurity Enthusiast_
