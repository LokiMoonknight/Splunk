# Splunk
Project Idea: Phishing Email -> Detection with Splunk

<ins>**Table of Contents:**</ins>

*  Project Overview

*  Project Relevance

*  Methodology

*  Results

*  Conclusion

*  References

1. **Project Overview:**

This project will explore the use of GoPhish and Splunk within the context of Incident Response. My project will take a practical, simulation-based approach by staging a phishing attack in a controlled virtual environment and demonstrating how security teams detect, investigate, and respond to such an attack using a Security Information and Event Management (SIEM) platform. The goal is to show how GoPhish and Splunk work together in an incident response context by simulatuing a phishing campaign capturing the resulting logs, and building detection dashboards and alert rules that mirror real SOC workflows.

2. **Project Relevance:**

**Why Phishing?**

Phishing is regularly ranked as the leading initial attack vector in cybersecurity incidents. According to the Verizon Data Breach Investigations Report (DBIR) a significant majority of breaches involve a human element. Most commonly a user clicking a malicious link or submitting credentials to a fake login page. So knowing and understanding how phisihing attacks work is important to building effective incident response skills.

**Why GoPhish?**

GoPhish is an open-source phishing framework used by security teams to conduct authorized phishing simulations. It allows experts to:

*  Design realistic phishing emails and fake login pages

*  Send campaigns to target accounts in a controlled environment

*  Track engagement metrics in real time

In incident response (IR) understanding attacker techniques is just as important a sknowing how to defend against them. GoPhish provides hands-on exposure to phishing mechanics without requiring advanced offensive security skills. 

**Why Splunk?**

Splunk is one of the most widely used SIEM platforms in enterprise security environments. SOC analysts use Splunk to:

*  Ingest and centralize logs from multiple sources (endpoints, network devices, applications)

*  Search and correlate events to identify indicators of compromise (IOCs)

*  Build dashboards for real-time visibility into the environment

*  Create automated alert rules that trigger on suspicious activity

**Skills Gained**

Working through this project provides hands-on expereince with:

*  Phishing attack mechanics and social engineering techniques

*  Log analysis and threat hunting using Splunk Search Processing Language (SPL)

*  Mapping real-world attacks to the NIST SP 800-61 Incident Response Lifecycle

*  Building detection dashboards and writing alert rules

*  Communicating technical findings to both technical and non-technical audiences

3. **Methodology:**

**Environment Setup**

| Component | Tool/Platform |
|-----------|---------------|
| Virtualization | VirtualBox |
| Victim Machine | Windows 10 VM |
| Phishing Framework | GoPhish |
| SIEM Platform | Splunk Free |
| Test Email Account | Dedicated Gmail account (victim) |

The lab runs within VirtualBox with the Windows VM acting as the simulated victim machine. GoPhish runs on the host machine and Splunk is installed on the Windows VM to inggest local logs.

**Tools, Frameworks & Datasets**

**Tools:**

*  GoPhish — Phishing simulation framework

*  Splunk Free — SIEM and log analysis platform

*  VirtualBox — Virtualization for isolated lab environment

**Frameworks:**

*  NIST SP 800-61 Rev. 2 — Incident Response Lifecycle

*  MITRE ATT&CK T1566 — Phishing technique classification

**Datasets (Primary — Self-Generated):**

*  GoPhish campaign logs (email opens, link clicks, credential submissions)

*  Windows Event Logs from victim VM

*  Network traffic logs from victim machine HTTP/HTTPS activity

*  Splunk query output and dashboard data

**Workflow / Data Pipeline**

```mermaid
graph TD;
  A["GoPhish Campaign"] --> B["Phishing Email Sent to Victim Account"];
  B --> C["Victim Clicks Link on Windows VM"];
  C --> D["Fake Login Page Served / Credentials Captured"];
  D --> E["Windows Event Logs + Network Traffic Generated"];
  E --> F["Logs Ingested into Splunk"];
  F --> G["SPL Queries Run — IOCs Identified"];
  G --> H["Dashboard Built + Alert Rule Created"];
  H --> I["Incident Mapped to NIST IR Lifecycle"];
```

**Step-by-Step Process**

**Phase 1 — Preparation (Week 1)**

1. Install VirtualBox and provision a Windows 10 VM

2. Install and configure GoPhish on the host machine
   
3.  Install Splunk Free on the Windows VM and configure log inputs
   
4. Create a test Gmail account to serve as the phishing victim

**Phase 2 — Attack Simulation (Week 2)**

1. In GoPhish, design a fake Microsoft 365 login page

2. Craft a phishing email ("Your password is expiring — update it now")
   
3. Launch the campaign targeting the test Gmail account
   
4. Open the email and click the link from within the Windows VM
   
5. Submit fake credentials on the fake login page
   
6. Document all GoPhish dashboard outputs (screenshots)

**Phase 3 — Detection & Analysis (Week 3)**

1. Confirm Windows Event Logs and network logs are flowing into Splunk
   
2. Run SPL queries to identify IOCs:

    * Suspicious outbound HTTP connections

    *  DNS queries to unknown domains

    *  Login events correlated with link-click timestamps

3. Build a Splunk dashboard visualizing the full incident timeline

4. Create an alert rule that fires on similar future activity

5. Map findings to the four NIST IR phases

**Phase 4 — Reporting & Presentation (Week 4)**

1. Finalize the written report
   
2. Record or rehearse the live demo
   
3. Build and rehearse the oral presentation

4. **Results:**
  <img width="975" height="580" alt="image" src="https://github.com/user-attachments/assets/12be18a2-ea4a-4820-944e-77b4915f6b38" />

![Alt Text](copied-url).

<img width="975" height="580" alt="image" src="https://github.com/user-attachments/assets/11223b13-abcb-463b-a985-7c7112d0b5b3" />

<img width="975" height="580" alt="image" src="https://github.com/user-attachments/assets/d80a3d74-fb85-4360-a1c0-4166b06b789f" />

<img width="975" height="580" alt="image" src="https://github.com/user-attachments/assets/63ea1b92-1b7b-42be-a37b-1d8223d22f00" />

<img width="975" height="580" alt="image" src="https://github.com/user-attachments/assets/128450cf-2909-4979-89b6-17f0a3ceacbb" />
  
<img width="975" height="506" alt="image" src="https://github.com/user-attachments/assets/162011e3-a3ae-461d-a562-05e76f45b1c1" />

<img width="975" height="506" alt="image" src="https://github.com/user-attachments/assets/90a6d208-d108-498e-afbf-359f91be48ae" />

<img width="975" height="506" alt="image" src="https://github.com/user-attachments/assets/afc9e7b4-c760-4232-b0b3-724a5022d78e" />

<img width="975" height="506" alt="image" src="https://github.com/user-attachments/assets/0e136583-e247-4972-9c6c-54e312fafd3e" />

<img width="975" height="507" alt="image" src="https://github.com/user-attachments/assets/f88bbd77-6cdc-40ca-8d86-4134c149f966" />

<img width="975" height="580" alt="image" src="https://github.com/user-attachments/assets/87642868-b22e-42f9-92a5-1479b818a9ec" />

<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/f2e2f291-9743-46f7-bee6-0cd270cb882a" />

<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/a7dbf132-c815-4822-bb64-c187b6744d95" />

<img width="975" height="507" alt="image" src="https://github.com/user-attachments/assets/7946584c-133c-4de4-8143-d83d839de5e4" />

<img width="975" height="506" alt="image" src="https://github.com/user-attachments/assets/bbee4b05-e480-46ea-b89d-a7c03e253b74" />

<img width="975" height="507" alt="image" src="https://github.com/user-attachments/assets/aad9e822-e384-4bed-aa2a-5cb930b507f5" />

<img width="975" height="513" alt="image" src="https://github.com/user-attachments/assets/f5b4e98a-0ebe-4123-9c0a-90f2199d22bb" />
