# 🔐 WEEK 02 – FOOTPRINTING, RECONNAISSANCE & NETWORK SCANNING

### Cybersecurity & Ethical Hacking Internship | NETWORKWALKS

**👤 Intern:** Saloni Kakkar  
**🎓 Batch:** B084 – NETWORKWALKS  
**📅 Week:** 02  
**🔍 Domain:** Cybersecurity & Ethical Hacking  
**🎯 Focus Areas:** Footprinting | OSINT | Reconnaissance | Network Scanning

---

# 📌 PROJECT OVERVIEW

This repository documents the practical activities completed during Week 02 of my Cybersecurity and Ethical Hacking Internship at NETWORKWALKS.

The primary objective was to understand footprinting and reconnaissance techniques used to gather publicly available information, investigate digital footprints, analyze domain infrastructure and identify active hosts within a network.

The practical work covered four modules using Kali Linux utilities, Maltego, theHarvester and Zenmap.

---

# 🎯 OBJECTIVES

- Understand the fundamentals of footprinting and reconnaissance.
- Gather domain registration and DNS-related information.
- Identify website technologies and server configurations.
- Perform OSINT investigations using Maltego.
- Collect publicly available information using theHarvester.
- Discover live hosts and visualize network topology using Zenmap.
- Analyze potential security exposures and preventive measures.

---

# 🛠️ TOOLS & TECHNOLOGIES USED

| Tool | Category | Purpose |
|---|---|---|
| 🐉 Kali Linux | Operating System | Cybersecurity testing environment |
| WHOIS | Footprinting | Domain registration information |
| WhatWeb | Fingerprinting | Website technology identification |
| Nslookup | DNS | Domain name resolution |
| cURL | Web Analysis | HTTP response header inspection |
| Wafw00f | Web Security | Web Application Firewall detection |
| DNSRecon | DNS | DNS record enumeration |
| Maltego | OSINT | Graphical link analysis and relationship mapping |
| theHarvester | OSINT | Email and subdomain information gathering |
| Nmap | Network Scanning | Host discovery and network scanning |
| Zenmap | Network Scanning | Graphical scanning and topology visualization |

---

# 🔍 MODULE 1 – FOOTPRINTING USING KALI LINUX TOOLS (W2-PM1)

## Overview

Footprinting is an initial phase of reconnaissance in cybersecurity. It involves collecting publicly available information about a target domain to understand its digital infrastructure, technologies, DNS configuration and security mechanisms.

**Target Domain:** `networkwalks.com`

## Tools and Commands

### 1. WHOIS – Domain Information Gathering

```bash
whois networkwalks.com
```

**Purpose:**
- Identify domain registration details.
- Examine registrar information.
- View registration and expiry information.
- Identify name servers.

### 2. WhatWeb – Technology Fingerprinting

```bash
whatweb networkwalks.com
```

**Purpose:**
- Identify website technologies.
- Detect CMS and web server information.
- Examine technology details exposed by the website.

### 3. Nslookup – DNS Resolution

```bash
nslookup networkwalks.com
```

**Purpose:**
- Resolve domain names into IP addresses.
- Examine DNS resolution information.

### 4. cURL – HTTP Header Analysis

```bash
curl -I https://networkwalks.com
```

**Purpose:**
- Retrieve HTTP response headers.
- Examine server response information.
- Understand information exposed through HTTP headers.

### 5. Wafw00f – Firewall Detection

```bash
wafw00f networkwalks.com
```

**Purpose:**
- Identify whether a Web Application Firewall protects the website.
- Understand the role of WAF in web application security.

### 6. DNSRecon – DNS Enumeration

```bash
dnsrecon -d networkwalks.com
```

**Purpose:**
- Enumerate DNS records.
- Examine name servers and mail server information.
- Identify available DNS records.

### 📊 Tools Summary

| No. | Tool | Information Gathered |
|---|---|---|
| 1 | WHOIS | Domain registration details |
| 2 | WhatWeb | Website technologies |
| 3 | Nslookup | Domain IP information |
| 4 | cURL | HTTP response headers |
| 5 | Wafw00f | WAF information |
| 6 | DNSRecon | DNS infrastructure |

### 💡 Learning Outcome

Gained practical understanding of domain footprinting, DNS enumeration, website technology fingerprinting, HTTP header analysis and firewall detection using Kali Linux.

---

# 🕸️ MODULE 2 – FOOTPRINTING WITH MALTEGO (W2-PM3)

## Overview

Maltego is an OSINT and graphical link-analysis tool used to investigate relationships between digital entities such as domains, email addresses, organizations and publicly available information.

**Target Domain:** `networkwalks.com`

### 🔧 Activities Performed

1. Downloaded and installed Maltego.
2. Completed the initial application configuration.
3. Created and logged into a Maltego account.
4. Created a new graph workspace.
5. Selected the Domain entity and added it to the workspace.
6. Configured the entity with `networkwalks.com`.
7. Explored available email-related transforms.
8. Executed relevant transforms to investigate associated information.

### 📊 Key Concepts

| Concept | Description |
|---|---|
| Entity | Represents information such as domains or email addresses |
| Transform | Retrieves related information from available data sources |
| Graph | Visually represents relationships between entities |
| OSINT | Gathering information from publicly available sources |

### 💡 Learning Outcome

Learned how Maltego supports OSINT investigations through entity creation, transformations and graphical relationship mapping.

---

# 📧 MODULE 3 – FOOTPRINTING WITH THEHARVESTER (W2-PM4)

## Overview

theHarvester is an information-gathering tool used to collect publicly available information such as email addresses, hostnames, IP addresses and subdomains from different OSINT sources.

**Target Domain:** `microsoft.com`

### 🔹 Practical – Information Gathering Using Baidu

**Command Executed:**

```bash
theHarvester -d microsoft.com -b baidu
```

### ⚙️ Command Explanation

| Parameter | Description |
|---|---|
| `theHarvester` | Launches the information-gathering tool |
| `-d` | Specifies the target domain |
| `microsoft.com` | Target domain |
| `-b` | Specifies the search source |
| `baidu` | Selected search engine |

### 📋 Information Gathering Capabilities

- Publicly available email addresses.
- Subdomains and hostnames.
- IP address information.
- Domain-related infrastructure information.

### 🔎 Observations

The practical demonstrated how theHarvester can collect publicly available information through search engine sources.

The Baidu search did not return email addresses, IP addresses or hostnames in the observed output.

### 💡 Learning Outcome

Understood domain-based information gathering, search engine data sources and the importance of passive reconnaissance.

---

# 🖥️ MODULE 4 – NETWORK SCANNING WITH ZENMAP (W2-PM5)

## Overview

Zenmap is the graphical interface of Nmap. It is used for network discovery, host identification and security auditing. It also provides a visual representation of discovered network devices.

### 🔧 Activities Performed

**Step 1 – Identify Local Network Configuration**

Used the Windows command:

```cmd
ipconfig
```

This helped identify the local IP configuration and network details.

**Step 2 – Identify Target Subnet**

```text
192.168.29.0/24
```

**Step 3 – Perform Host Discovery**

```bash
nmap -sn 192.168.29.0/24
```

### ⚙️ Command Explanation

| Parameter | Description |
|---|---|
| `nmap` | Starts the Nmap scanning tool |
| `-sn` | Performs host discovery without port scanning |
| `192.168.29.0/24` | Specifies the target subnet |

### 📊 Network Scan Results

| Parameter | Observed Result |
|---|---|
| Target Network | 192.168.29.0/24 |
| Scan Type | Ping Scan |
| Total IP Addresses | 256 |
| Active Hosts Identified | 3 |
| Scan Duration | 3.26 seconds |
| Nmap Version | 7.99.3 |

### 🖧 Discovered Hosts

| No. | IP Address / Hostname | Status |
|---|---|---|
| 1 | 192.168.29.1 (reliance.reliance) | 🟢 Active |
| 2 | 192.168.29.37 | 🟢 Active |
| 3 | 192.168.29.230 | 🟢 Active |

### 🔍 MAC Address Information

| IP Address | MAC Address |
|---|---|
| 192.168.29.1 | A8:88:1F:A4:86:8C |
| 192.168.29.37 | AA:BA:67:2E:11:54 |
| 192.168.29.230 | Not available in captured output |

### 🗺️ Network Topology Visualization

After completing the scan:

1. Opened the Topology tab in Zenmap.
2. Enabled the topology legend.
3. Reviewed the graphical representation of discovered hosts.
4. Examined the connections displayed in the topology.
5. Saved the network topology in PDF format.

### 💡 Learning Outcome

Gained practical experience in network scanning, live host discovery, IP and MAC address identification and network topology visualization.

---

# ⚠️ OVERALL RISK ANALYSIS

The following table summarizes potential security considerations associated with the techniques explored during the practical exercises.

| No. | Finding | Potential Impact | Risk Level |
|---|---|---|---|
| 1 | Public domain information | May assist infrastructure reconnaissance | Low |
| 2 | Website technology exposure | May help identify outdated technologies | Medium |
| 3 | DNS information exposure | May reveal infrastructure details | Medium |
| 4 | Public email information | Could be misused for phishing | Medium |
| 5 | Multiple active network hosts | Unknown devices may require investigation | Medium |

*Note: These are potential security risks, not confirmed vulnerabilities.*

---

# 🛡️ SECURITY RECOMMENDATIONS

1. **Strong Authentication:** Use strong passwords and appropriate authentication mechanisms.
2. **Software Updates:** Keep website technologies, plugins and server components updated.
3. **DNS Security:** Review DNS configurations and remove unnecessary records.
4. **Email Protection:** Implement anti-phishing measures.
5. **Network Monitoring:** Regularly identify and investigate unknown devices.
6. **Firewall Configuration:** Maintain appropriate firewall and access-control policies.
7. **Authorized Testing:** Perform security testing only within an approved scope.

---

# 🧠 KEY LEARNINGS

During these practical modules, I gained hands-on experience in:

- Footprinting and passive reconnaissance.
- Domain registration and DNS information gathering.
- Website technology fingerprinting.
- HTTP response header analysis.
- Web Application Firewall detection.
- OSINT and graphical link analysis using Maltego.
- Email and subdomain information gathering using theHarvester.
- Network discovery using Nmap and Zenmap.
- Live host identification and topology visualization.
- Technical documentation and security analysis.

---

# 📸 EVIDENCE & SCREENSHOTS

The following evidence demonstrates the practical network scanning activities.

### 🖼️ Evidence 01 – Zenmap Network Topology

![Zenmap Network Topology](Evidence/zenmap_topology.png)

*Figure 1: Network topology showing discovered hosts.*

### 🖼️ Evidence 02 – Nmap Scan Results

![Nmap Scan Results](Evidence/nmap_scan.png)

*Figure 2: Nmap ping scan showing three active hosts.*

### 📄 Evidence 03 – Saved Network Topology

[📥 View Network Topology PDF](Evidence/nmap.pdf)

Additional screenshots for PM1, PM3 and PM4 can be organized in their respective evidence folders.

---

# 🏁 CONCLUSION

During Week 02 of my Cybersecurity and Ethical Hacking internship at NETWORKWALKS, I completed practical activities covering footprinting, reconnaissance, OSINT and network scanning.

I explored six Kali Linux tools, investigated domain relationships using Maltego, performed information gathering with theHarvester and conducted network discovery using Zenmap.

The network scanning practical successfully identified three active hosts within my local network and provided a graphical representation of the discovered devices.

Overall, these activities strengthened my understanding of reconnaissance methodologies, information-gathering techniques and network discovery tools used in cybersecurity assessments.

---

# 📚 REFERENCES

| Resource | Documentation |
|---|---|
| NETWORKWALKS | [Official Website](https://networkwalks.com/) |
| Kali Linux | [Official Documentation](https://www.kali.org/docs/) |
| Nmap | [Reference Guide](https://nmap.org/book/man.html) |
| Zenmap | [Official Documentation](https://nmap.org/zenmap/) |
| Maltego | [Documentation](https://docs.maltego.com/) |
| theHarvester | [GitHub Repository](https://github.com/laramies/theHarvester) |
| DNSRecon | [GitHub Repository](https://github.com/darkoperator/dnsrecon) |
| Wafw00f | [GitHub Repository](https://github.com/EnableSecurity/wafw00f) |

---

# 👩‍💻 AUTHOR

**Saloni Kakkar**

🎓 Cybersecurity & Ethical Hacking Intern  
🏢 NETWORKWALKS  
📌 Batch: B084

**Focus Areas:** Cybersecurity | Ethical Hacking | OSINT | Penetration Testing | Network Security

---

# ⚖️ DISCLAIMER

This repository is created strictly for educational and learning purposes as part of a cybersecurity internship.

All network scanning activities documented here were conducted on my own local network. Reconnaissance and scanning should only be performed on systems and networks where appropriate authorization has been obtained.

The documented activities represent practical learning exercises and do not constitute a complete penetration test or independently verified security audit.

---

⭐ **Thank you for visiting my Week 02 cybersecurity repository!**

`#CyberSecurity` `#EthicalHacking` `#KaliLinux` `#OSINT` `#Nmap` `#Zenmap` `#Maltego` `#PenetrationTesting`
