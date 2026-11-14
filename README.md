
# 🔐 WEEK 2 – CYBERSECURITY & ETHICAL HACKING
## Footprinting, Reconnaissance & Network Scanning

**Internship Program:** NETWORKWALKS  
**Batch:** B084  
**Week:** 02  
**Domain:** Cybersecurity & Ethical Hacking  
**Author:** Saloni Kakkar  
**Tools:** Kali Linux, Maltego, theHarvester, Zenmap, Nmap  
**Platform:** GitHub

---

# 📌 1. Project Overview

This repository documents my Week 2 practical activities as part of the Cybersecurity Internship Program at NETWORKWALKS.

The main objective of this week's activities was to understand how cybersecurity professionals perform information gathering, footprinting, reconnaissance, and network scanning using different cybersecurity tools.

I explored multiple tools available in Kali Linux and learned how to identify publicly available information, investigate domain-related data, and discover active devices on a local network.

The practical activities helped me understand how reconnaissance and scanning are performed before moving towards vulnerability assessment and penetration testing.

---

# 🎯 2. Objectives

The objectives of this week's practical work were:

- Understand the fundamentals of footprinting and reconnaissance.
- Learn how to collect publicly available information about a target.
- Explore different Kali Linux information-gathering tools.
- Understand Google Hacking Database (GHDB) and search operators.
- Learn how to perform footprinting using Maltego.
- Discover email addresses and subdomains using theHarvester.
- Understand network discovery using Nmap and Zenmap.
- Identify active hosts within a local network.
- Generate and interpret a network topology.
- Document practical activities and their observations.

---

# 🛠️ 3. Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Linux distribution used for cybersecurity practicals |
| WHOIS | Collect domain registration information |
| WhatWeb | Identify website technologies |
| Nslookup | Resolve domain names into IP addresses |
| Curl | Inspect HTTP response headers |
| Wafw00f | Identify Web Application Firewall technologies |
| DNSRecon | Enumerate DNS records |
| GHDB | Explore Google Dorks and advanced search operators |
| Maltego | Visualize relationships between domains, people, infrastructure and other entities |
| theHarvester | Gather publicly available email addresses and subdomains |
| Nmap | Discover hosts and scan networks |
| Zenmap | Graphical interface for Nmap |
| Windows CMD | Identify local network configuration using ipconfig |

---

# 📚 4. Practical Activities Performed

## 4.1 W2-PM1 – Footprinting Using Multiple Kali Linux Tools

**Objective:** To understand how different Kali Linux tools can be used to gather information about a target domain.

I explored multiple tools to understand the different stages of information gathering.

### Tools and their functions

| Tool | Command | Information Collected |
|---|---|---|
| WHOIS | `whois domain.com` | Domain registration details |
| WhatWeb | `whatweb domain.com` | Website technologies and CMS |
| Nslookup | `nslookup domain.com` | Domain IP resolution |
| Curl | `curl -I https://domain.com` | HTTP response headers |
| Wafw00f | `wafw00f domain.com` | Web Application Firewall detection |
| DNSRecon | `dnsrecon -d domain.com` | DNS records and infrastructure information |

### Learning Outcomes

- Understood domain registration information.
- Learned website technology fingerprinting.
- Understood DNS resolution.
- Learned how to inspect HTTP response headers.
- Explored WAF detection.
- Understood DNS enumeration.

These tools demonstrated how different information-gathering techniques contribute to the reconnaissance phase.

---

## 4.2 W2-PM2 – Google Hacking Database (GHDB)

**Status: Not Completed**

GHDB was part of the assigned practical activities but was not completed during this submission.

### Objective

To understand how Google advanced search operators, also known as Google Dorks, can help identify publicly indexed information.

### Concepts to Study

| Search Operator | Purpose |
|---|---|
| `site:` | Restrict search results to a particular website |
| `filetype:` | Search for a specific file format |
| `intitle:` | Search for terms appearing in page titles |
| `inurl:` | Search for terms appearing in URLs |
| `intext:` | Search for specific text within page content |

### Learning Outcome

Understood the basic concept of Google Dorks and how search operators can be used during passive reconnaissance.

**Note:** The practical GHDB activity remains pending and is not claimed as completed.

---

## 4.3 W2-PM3 – Footprinting Using Maltego

**Objective:** To understand how Maltego can be used for visual information gathering and relationship mapping.

Maltego is an open-source intelligence (OSINT) tool that helps visualize connections between different entities.

### Key Concepts

- Entity creation
- Domain investigation
- Relationship mapping
- Transformations
- Infrastructure visualization
- OSINT-based reconnaissance

### Learning Outcomes

- Understood the Maltego interface.
- Explored how entities represent different types of information.
- Learned how transformations can retrieve related information.
- Understood how visual graphs help in analyzing relationships.

---

## 4.4 W2-PM4 – Footprinting Using theHarvester

**Objective:** To collect publicly available information related to a target organization using theHarvester in Kali Linux.

### Command Used

```bash
theHarvester -d microsoft.com -b baidu
```

### Command Explanation

| Parameter | Explanation |
|---|---|
| `theHarvester` | Starts the information-gathering tool |
| `-d` | Specifies the target domain |
| `microsoft.com` | Target domain |
| `-b` | Specifies the search source |
| `baidu` | Search engine used as the data source |

### Information Gathering

TheHarvester can help discover:

- Publicly available email addresses
- Subdomains
- Hostnames
- Related infrastructure information

### Learning Outcomes

- Learned how to execute theHarvester.
- Understood domain-based information gathering.
- Explored the use of different search sources.
- Understood the importance of passive reconnaissance.

---

## 4.5 W2-PM5 – Network Scanning Using Zenmap

**Objective:** To discover active devices on my local network, identify their IP addresses, and visualize the network topology using Zenmap.

For this activity, I used Zenmap, which provides a graphical interface for Nmap.

### Step 1: Identify the Target Network

I selected my local network subnet:

```bash
192.168.29.0/24
```

### Step 2: Perform a Ping Scan

**Command executed:**

```bash
nmap -sn 192.168.29.0/24
```

### Command Explanation

| Parameter | Explanation |
|---|---|
| `nmap` | Starts the Nmap network scanning tool |
| `-sn` | Performs host discovery without a port scan |
| `192.168.29.0/24` | Specifies the target subnet |

### Step 3: Scan Results

The scan successfully discovered three active hosts.

**Actual scan information:**

| Parameter | Result |
|---|---|
| Target Network | `192.168.29.0/24` |
| Scan Type | Ping Scan |
| Nmap Command | `nmap -sn 192.168.29.0/24` |
| Total IP Addresses Scanned | 256 |
| Live Hosts Found | 3 |
| Scan Duration | 3.26 seconds |
| Nmap Version | 7.99.3 |

### Step 4: Live Hosts Discovered

| S.No. | Hostname / IP Address | Status |
|---|---|---|
| 1 | `192.168.29.1` (reliance.reliance) | Active |
| 2 | `192.168.29.37` | Active |
| 3 | `192.168.29.230` | Active |

All three discovered hosts responded during the host discovery scan.

### Step 5: MAC Address Information

The scan also displayed MAC address information for discovered devices where available.

| IP Address | MAC Address |
|---|---|
| `192.168.29.1` | `A8:88:1F:A4:86:8C` |
| `192.168.29.37` | `AA:BA:67:2E:11:54` |
| `192.168.29.230` | Not displayed in the captured output |

### Step 6: Network Topology

After completing the scan, I opened the **Topology** tab in Zenmap.

The topology visualization displayed the localhost connection and the three discovered network hosts.

I also opened the topology legend to understand the different host and connection indicators.

### Network Topology Observations

- Three active hosts were identified.
- The localhost node was displayed in the topology.
- The discovered devices were represented as separate nodes.
- Dashed connections indicated that traceroute information was unavailable.
- The topology helped visualize the discovered network devices.

---

# 📸 5. Practical Evidence & Screenshots

The following screenshots demonstrate my actual Zenmap practical work.

## Evidence 1 – Zenmap Network Topology

This screenshot shows the topology generated after scanning my local network.

![Zenmap Network Topology](Screenshot%202026-11-13%20213704.png)

**Observation:** Three active hosts were successfully identified and represented in the network topology.

## Evidence 2 – Nmap Ping Scan Output

This screenshot displays the actual Nmap command and its output.

![Nmap Scan Output](Screenshot%202026-11-13%20213724.png)

**Observation:**

- Target subnet: `192.168.29.0/24`
- Three hosts found up.
- 256 IP addresses scanned.
- Total scanning time: 3.26 seconds.

## Evidence 3 – Saved Network Topology

The network topology was also saved as a PDF for documentation.

[View Zenmap Network Topology PDF](nmap.pdf)

---

# 🔍 6. Findings & Observations

Based on the completed practical activities, the following observations were made.

| No. | Activity | Observation | Significance |
|---|---|---|---|
| 1 | WHOIS | Explored domain registration information | Helps understand domain ownership and registration |
| 2 | WhatWeb | Explored website technology fingerprinting | Helps identify exposed technologies |
| 3 | Nslookup | Learned domain-to-IP resolution | Helps identify network destinations |
| 4 | Curl | Inspected HTTP response headers | Helps understand web server responses |
| 5 | Wafw00f | Explored WAF detection | Helps identify security technologies |
| 6 | DNSRecon | Explored DNS enumeration | Helps understand DNS infrastructure |
| 7 | Maltego | Explored visual OSINT investigation | Helps map relationships between entities |
| 8 | theHarvester | Performed domain-based information gathering | Helps discover publicly available information |
| 9 | Zenmap | Discovered three active local network hosts | Helps understand network visibility |
| 10 | GHDB | Practical activity not completed | Remains pending |

---

# ⚠️ 7. Risk Analysis

Information gathered during reconnaissance and network scanning can help security professionals understand the exposure of a system.

The following table describes potential risks associated with the observations.

| No. | Finding | Potential Risk | Risk Level |
|---|---|---|---|
| 1 | Publicly available domain information | May reveal infrastructure-related details | Low |
| 2 | Website technology fingerprinting | May help identify outdated technologies | Medium |
| 3 | DNS information exposure | May reveal infrastructure details | Medium |
| 4 | Publicly available email addresses | May be misused for phishing attempts | Medium |
| 5 | Multiple active network hosts | Unknown devices may require investigation | Medium |
| 6 | Network information exposure | May assist further reconnaissance | Low |

**Important:** These are potential risks, not confirmed vulnerabilities. No exploitation or unauthorized access was performed as part of the documented activities.

---

# 🛡️ 8. Security Recommendations

Based on the concepts explored during these activities, the following security recommendations are suggested:

1. Regularly review publicly exposed domain and infrastructure information.
2. Keep website technologies, CMS platforms, and plugins updated.
3. Review DNS configurations and remove unnecessary records.
4. Protect publicly available organizational email addresses from misuse.
5. Regularly monitor network-connected devices.
6. Investigate unknown or unexpected devices.
7. Maintain updated network documentation.
8. Use appropriate firewall and security configurations.
9. Perform reconnaissance and scanning only with proper authorization.

---

# 📖 9. Learning Outcomes

During Week 2, I gained practical exposure to several cybersecurity concepts.

### Technical Skills

- Linux-based information gathering.
- Domain footprinting and reconnaissance.
- DNS enumeration and resolution.
- Website technology identification.
- OSINT investigation using Maltego.
- Email and subdomain discovery using theHarvester.
- Network discovery using Nmap.
- Network topology visualization using Zenmap.
- Understanding Google Dorking concepts.

### Practical Understanding

I learned that reconnaissance is an important stage of penetration testing because it helps security professionals understand a target environment before conducting further security assessments.

I also understood the importance of interpreting scan results instead of simply executing commands.

---

# 📝 10. Conclusion

Week 2 of my Cybersecurity Internship at NETWORKWALKS helped me develop a better understanding of footprinting, reconnaissance, OSINT, and network scanning.

I explored different Kali Linux tools and their applications in information gathering. I also learned how Maltego can visualize relationships between entities and how theHarvester can collect publicly available information.

One of the important practical activities was network discovery using Zenmap. I successfully scanned my local network using Nmap and identified three active hosts within the `192.168.29.0/24` subnet. I also generated a network topology to visualize the discovered devices.

Although the GHDB practical activity remains incomplete, I gained an understanding of the basic Google search operators used in passive reconnaissance.

Overall, these activities improved my understanding of how cybersecurity professionals approach information gathering and network discovery.

---

# 📂 11. Repository Structure

```text
Week-2-Cybersecurity/
│
├── README.md
│
├── Screenshot 2026-11-13 213704.png
│
├── Screenshot 2026-11-13 213724.png
│
└── nmap.pdf
```

---

# ⚖️ 12. Disclaimer

All network scanning activities documented in this repository were performed on my own local network for educational purposes.

Reconnaissance and scanning should only be performed on systems, networks, and domains for which proper authorization has been obtained.

This repository is intended for cybersecurity education, learning, and documentation purposes only.

---

# 👩‍💻 13. Author

**Saloni Kakkar**  
Cybersecurity & Ethical Hacking Intern  
NETWORKWALKS – Batch B084

**Week:** 02  
**Repository:** GitHub  
**Focus Areas:** Cybersecurity | Ethical Hacking | OSINT | Footprinting | Network Scanning | Penetration Testing

---

⭐ Thank you for visiting my Week 2 cybersecurity practical repository!

#CyberSecurity #EthicalHacking #KaliLinux #Nmap #Zenmap #OSINT #Footprinting #NetworkScanning #PenetrationTesting #NETWORKWALKS
