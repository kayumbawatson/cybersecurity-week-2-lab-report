
# PENETRATION TESTING REPORT
### FOOTPRINTING, RECONNAISSANCE & NETWORK SCANNING

**W2-PM-FINAL  |  CYBERSECURITY  |  NETWORKWALKS**

| Field | Detail |
|---|---|
| **Pentester Name (Cybersecurity Professional)** | **Watson Kayumba** |
| **Program/Batch** | B084-Networkwalks |
| **Date** | 14th November, 2026 |
| **Modules Completed** | W2-PM3 – Footprinting with Maltego<br>W2-PM4 – Footprinting & Reconnaissance with theHarvester<br>W2-PM5 – Network Scanning with Zenmap |
| **Client/Target** | 1. `networkwalks.com` (authorized Maltego exercise)<br>2. My own local LAN<br>3. `microsoft.com` (theHarvester exercise) |
| **Permission Secured from Client?** | Yes – within the assigned scope: authorized target domain and my own local LAN. The `microsoft.com` exercise used publicly available sources only. |
| **Phases Covered** | **Phase 1:** Footprinting & Reconnaissance<br>**Phase 2:** Network Scanning & Host Discovery |

---

# 1. Liability Disclaimer

I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.

# 2. Introduction

This report documents three practical cybersecurity labs completed as part of the Networkwalks Cybersecurity programme: footprinting with Maltego, network scanning with Zenmap, and footprinting and reconnaissance with theHarvester. The exercises focused on discovering publicly available information about specified domains and identifying active devices on my own local area network.

The assigned targets and scope were `networkwalks.com` for the Maltego exercise (with permission), my own local LAN for the Zenmap exercise, and `microsoft.com` for theHarvester exercises. The report describes the tasks and tool configurations used. Actual results such as discovered email addresses, subdomains, host addresses and MAC addresses should be entered from my own tool output and supported with screenshots in the evidence section.

# 3. Tools Used

The table below lists each tool used in this report and its purpose.

| Tool / Source | Purpose |
|---|---|
| **Kali Linux** | Operating system used to run the footprinting and reconnaissance tools. |
| **Maltego** | Visual footprinting and link analysis to identify email addresses associated with `networkwalks.com`. |
| **Zenmap (Nmap GUI)** | Discover live hosts on my own LAN, identify IP and MAC addresses, and display the network topology. |
| **theHarvester** | Gather publicly available email IDs and subdomains associated with `microsoft.com`. |
| **Baidu** | Search source specified for the first theHarvester task; result limit set to 1,000. |
| **All sources** | Source selection specified for the second theHarvester task; result limit set to 50. |

# 4. Activities Performed

## 4.1 Footprinting with Maltego

I used Maltego to perform footprinting on the `networkwalks.com` domain. The assigned task was to find email addresses related to the target organization's domain. This exercise was carried out within the authorized scope provided for the lab.

The purpose of the exercise was to use Maltego's information-gathering and link-analysis capabilities to identify email addresses associated with `networkwalks.com`. I reviewed the information returned by the tool and used the results as evidence of the domain-footprinting process.

**Actual finding:** [Enter the number of email addresses identified and list the addresses or summarize them as appropriate. Include only results visible in your Maltego output.]

**Sources / transforms used:** [Enter the Maltego transforms or data sources you actually ran, if shown in your lab output.]

The results should be interpreted as publicly discoverable information. The exercise did not involve accessing email accounts or attempting to authenticate to any system.

The activity demonstrated how domain-related information can be collected and visually organized to support the reconnaissance phase of a security assessment.

All activity was limited to the assigned `networkwalks.com` target and the permission granted for this practical.

## 4.2 Network Scanning with Zenmap

For this practical, I used Zenmap to scan my own local area network. The assigned tasks were to identify my local IP address and LAN subnet, discover the live hosts on the subnet, count the live hosts, record their IP and MAC addresses, and save the network topology in PDF format on the desktop.

I first checked the network configuration on my computer to identify the local IP address and subnet information. I then entered my LAN subnet as the target in Zenmap and performed the assigned host-discovery scan.

The scan results should be recorded below using the values from my own Zenmap output:

- **Local IP address:** [Insert actual local IP address]
- **LAN subnet / network range:** [Insert actual subnet, e.g. the range shown by your configuration]
- **Total live hosts discovered:** [Insert actual count]
- **Live host IP addresses:** [List all IP addresses returned by your scan]
- **MAC addresses:** [List the corresponding MAC addresses shown in Zenmap]

I opened the **Topology** tab in Zenmap, displayed the network map and legend, and saved/exported the topology in PDF format to the desktop as required by the task.

**Saved PDF filename:** [Insert the saved PDF filename.]

**Note:** Do not use the example IP addresses or MAC addresses from the instructor's sample report. Replace these fields with the results from my own local network scan.

## 4.3 Footprinting & Reconnaissance with theHarvester

I used theHarvester in Kali Linux to search for email IDs and subdomains associated with the target organization `microsoft.com`. The practical contained two separate search tasks with different source selections and result limits.

### Task 1 – Search Using Baidu

For the first task, I configured theHarvester to search `microsoft.com` using Baidu as the source and set the maximum number of results to 1,000, as specified in the lab.

**Results:** [Insert the email IDs and subdomains returned by your Baidu search, or summarize the totals. Record zero results if none were returned.]

### Task 2 – Search Using All Sources

For the second task, I ran theHarvester against `microsoft.com` using all available sources and set the result limit to 50, as specified in the lab.

**Results:** [Insert the email IDs and subdomains returned by the all-sources search, or summarize the totals. Record zero results if none were returned.]

The two searches demonstrate that the information returned by a footprinting tool can vary depending on the selected data sources and result limit. Results should be treated as publicly sourced information and may be incomplete or outdated.

# 5. Risk Analysis / Impact

The following table outlines potential security considerations related to the information gathered during the three practical exercises. These are observations and possible impacts, not confirmed vulnerabilities.

| # | Risk / Finding | Evidence / Observation | Potential Impact | Risk Level |
|---|---|---|---|---|
| 1 | Email addresses publicly discoverable | Maltego results for `networkwalks.com`: `info@networkwalks.com` | Publicly listed addresses may be targeted by spam or phishing attempts. | **Low** |
| 2 | Email IDs and subdomains discoverable from Baidu | theHarvester – `microsoft.com`, Baidu, limit 1,000 | Discovered information may assist further mapping and targeted social engineering. | **Medium** |
| 3 | Email IDs and subdomains discoverable from multiple sources | theHarvester – `microsoft.com`, all sources, limit 50 | Aggregated public information may provide a broader view of an organization's online presence. | **Medium** |
| 4 | Live devices visible on local network | Zenmap identified 2 live hosts on `192.168…./24`. | Unexpected or unauthorized devices, if present, may increase network exposure. | **Medium** |
| 5 | Device addressing information identified | IP and MAC addresses recorded from the actual Zenmap scan | Address information can support network mapping; it does not by itself establish a vulnerability. | **Informational** |

Risk ratings should be assigned only after reviewing the actual evidence and the context of the target environment. The lab outputs alone may not be sufficient to determine severity.

The findings in this report are observations from footprinting and host-discovery exercises, not confirmed vulnerabilities.

The practical exercises involved information gathering and local network discovery. No exploitation, credential attacks or vulnerability validation was performed as part of the assigned tasks.

A discovered email address, subdomain, live host, IP address or MAC address does not by itself prove that a system is vulnerable. Further assessment would require a defined scope and explicit authorization.

# 6. Recommendations

Based on the activities and observations from these labs, I recommend the following:

1. **Review publicly discoverable contact information**

   Organizations should understand which email addresses are publicly available and apply appropriate spam filtering, phishing awareness and account-security controls.

2. **Review public domain information**

   Organizations should periodically review publicly exposed domain-related information and correct outdated or unnecessary records where appropriate.

3. **Maintain an accurate network inventory**

   Network administrators should keep records of authorized devices, IP addresses and MAC addresses connected to the local network.

4. **Investigate unfamiliar devices**

   Unexpected live hosts discovered during network scans should be verified and investigated by the network owner.

5. **Secure local network access**

   Use strong Wi-Fi security, change default device credentials and restrict access to authorized users and devices.

6. **Keep network topology documentation current**

   Document the LAN subnet, connected devices and network topology, and update the records when changes occur.

7. **Validate and document reconnaissance results**

   Record the tool, target, source selection, result limit and actual output. Distinguish verified findings from assumptions or sample data.

8. **Perform authorized security testing only**

   Footprinting and scanning should be conducted only on systems and networks within an approved scope.

# 7. Conclusion

During the practical sessions, I completed three labs covering footprinting, reconnaissance and network scanning using Maltego, Zenmap and theHarvester.

In the Maltego lab, I investigated the `networkwalks.com` domain, within the authorized scope, to identify email addresses related to the target organization. This introduced me to visual link analysis as part of domain footprinting.

In the Zenmap lab, I identified my local IP address and LAN subnet, discovered live hosts, recorded the number of hosts and their IP and MAC addresses, and saved the network topology as a PDF.

In the theHarvester lab, I searched for email IDs and subdomains associated with `microsoft.com`. I performed one search using Baidu with a result limit of 1,000 and another using all available sources with a result limit of 50.

These exercises helped me understand how footprinting tools gather and organize publicly available information, while network-scanning tools identify active devices on an authorized local network. I also learned that results depend on tool configuration and data-source coverage.

Finally, I learned the importance of documenting the scope, configuration, actual findings and supporting evidence. Reconnaissance and scanning must always be performed responsibly and within the authorization provided.

# 8. Evidences Collected

The following screenshots provide supporting evidence of the practical activities performed.

### Evidence 1 – Maltego

Screenshot of the `networkwalks.com` investigation showing the email-address findings.

![Evidence 1 – Maltego](evidence/01-Maltego/maltego-results.png)

### Evidence 2 – Zenmap Network Scan

Screenshot showing the local network scan, discovered live hosts, and relevant IP and MAC address information.

![Evidence 2 – Zenmap Scan](evidence/02-Zenmap/zenmap-scan.png)

### Evidence 3 – Zenmap Network Topology

Screenshot of the network topology generated using Zenmap.

![Evidence 3 – Zenmap Topology](evidence/02-Zenmap/zenmap-topology.png)

### Evidence 4 – theHarvester (Baidu)

Screenshot showing the Baidu source configuration and the results returned for `microsoft.com`.

![Evidence 4 – theHarvester Baidu](evidence/03-theHarvester-Baidu/baidu-results.png)

### Evidence 5 – theHarvester (All Sources)

Screenshot showing the all-sources configuration and the resulting output for `microsoft.com`.

![Evidence 5 – theHarvester All Sources](evidence/04-theHarvester-All-Sources/all-sources-output.png)

---

**END OF REPORT**

*Prepared by Watson Kayumba | B084-Networkwalks*
