# Splunk
Project Idea: Phishing Email -> Detection with Splunk

<ins>Table of Contents:</ins>

• Project Overview

• Project Relevance

• Methodology

• Results

• Conclusion

• References

1. Project Overview:

This project will explore the use of GoPhish and Splunk within the context of Incident Response. My project will take a practical, simulation-based approach by staging a phishing attack in a controlled virtual environment and demonstrating how security teams detect, investigate, and respond to such an attack using a Security Information and Event Management (SIEM) platform. The goal is to show how GoPhish and Splunk work together in an incident response context by simulatuing a phishing campaign capturing the resulting logs, and building detection dashboards and alert rules that mirror real SOC workflows.

2. Project Relevance:

Why Phishing?

Phishing is regularly ranked as the leading initial attack vector in cybersecurity incidents. According to the Verizon Data Breach Investigations Report (DBIR) a significant majority of breaches involve a human element. Most commonly a user clicking a malicious link or submitting credentials to a fake login page. So knowing and understanding how phisihing attacks work is important to building effective incident response skills.

Why GoPhish?

GoPhish is an open-source phishing framework used by security teams to conduct authorized phishing simulations. It allows experts to:

• Design realistic phishing emails and fake login pages

• Send campaigns to target accounts in a controlled environment

• Track engagement metrics in real time

In incident response (IR) understanding attacker techniques is just as important a sknowing how to defend against them. GoPhish provides hands-on exposure to phishing mechanics without requiring advanced offensive security skills. 

Why Splunk?

Splunk is one of the most widely used SIEM platforms in enterprise security environments. SOC analysts use Splunk to:

• Ingest and centralize logs from multiple sources (endpoints, network devices, applications)

• Search and correlate events to identify indicators of compromise (IOCs)

• Build dashboards for real-time visibility into the environment

• Create automated alert rules that trigger on suspicious activity

Skills Gained

Working through this project provides hands-on expereince with:

• Phishing attack mechanics and social engineering techniques

• Log analysis and threat hunting using Splunk Search Processing Language (SPL)

• Mapping real-world attacks to the NIST SP 800-61 Incident Response Lifecycle

• Building detection dashboards and writing alert rules

• Communicating technical findings to both technical and non-technical audiences

3. Methodology

Environment Setup

| Component | Tool/Platform |
|-----------|---------------|
| Virtualization | VirtualBox |
| Victim Machine | Windows 11 VM |
| Phishing Framework | GoPhish |
| SIEM Platform | Splunk Free |
| Test Email Account | Dedicated Gmail account (victim) |

The lab runs within VirtualBox with the Windows VM acting as the simulated victim machine. GoPhish runs on the host machine and Splunk is installed on the Windows VM to inggest local logs.
