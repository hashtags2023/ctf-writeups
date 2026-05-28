# Defensive Security Intro — TryHackMe

**Date:** 2026-05-28
**Platform:** TryHackMe
**Path:** Cyber Security 101 — Section 1
**Difficulty:** Easy
**Room URL:** https://tryhackme.com/room/defensivesecurityintro

---

## Room Summary

An introduction to defensive security through a simulated SOC analyst scenario. Played the role of Joe, an apprentice SOC analyst on his first solo shift, investigating a live attack using a monitoring dashboard.

---

## What I Did

Worked through a 4-task scenario simulating a real SOC workflow:

1. **Learned what defensive security is** — monitoring, detecting, and responding to attacks rather than launching them
2. **Opened a monitoring dashboard** and reviewed active alerts to identify suspicious traffic
3. **Investigated the attack** — used the URL Discovery Attempts log to determine the attacker was doing directory enumeration (trying to find hidden pages on a website)
4. **Contained the attack** — blocked the attacker's IP via a firewall rule, applied rate limiting, and updated security rules

---

## Commands / Tools Used

- Monitoring dashboard (browser-based SOC simulation)
- Firewall rule management (IP block via dashboard UI)
- URL Discovery Attempts log (attacker enumeration history)

---

## Key Takeaways

1. **Defensive security = detect, investigate, respond.** You're not breaking into systems — you're watching for when others try to.

2. **SOC analysts work from dashboards.** Tools like SIEM dashboards surface suspicious activity so analysts don't have to read raw logs manually. LogSentinel does a simplified version of exactly this.

3. **Containment first, investigation second.** The priority when an attack is happening is to stop the bleeding — block the IP, apply rate limiting — then dig into the details after.

4. **Directory enumeration is noisy.** The attacker was rapidly hitting many URLs trying to find hidden pages. This is exactly the kind of pattern LogSentinel's scanner detection module catches in Apache/Nginx logs.

5. **The SOC workflow in this room maps directly to real tools:**
   - Dashboard alerts → SIEM (Splunk, Security Onion)
   - IP blocking → Firewall / fail2ban
   - URL discovery logs → Web access logs (what LogSentinel parses)

---

## Connection to My Projects

This room directly reinforced what I built in **LogSentinel** — specifically the scanner detection and web attack modules. The "URL Discovery Attempts" the attacker was making would show up in an Apache access log as rapid 404s from a single IP, which LogSentinel flags as reconnaissance activity.

Next step: run Gobuster against my own Metasploitable VM in my home lab and watch LogSentinel catch it in the access log.

---

## Resources

- [TryHackMe — Defensive Security Intro](https://tryhackme.com/room/defensivesecurityintro)
- [What is a SOC? — CrowdStrike](https://www.crowdstrike.com/cybersecurity-101/security-operations-center-soc/)
- [fail2ban docs](https://www.fail2ban.org/wiki/index.php/Main_Page)
