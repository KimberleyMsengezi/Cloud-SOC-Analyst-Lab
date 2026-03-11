# 01 - Cloud-Native SOC Lab | Microsoft Sentinel (Azure)

![Microsoft Sentinel](https://img.shields.io/badge/Microsoft%20Sentinel-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![KQL](https://img.shields.io/badge/KQL-Querying-FF6A00?style=for-the-badge)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-v15-red?style=for-the-badge)

## Overview
Built and operated a **full cloud-native Security Operations Center** using Microsoft Sentinel on Azure. Ingested multi-source logs, enabled AI-driven detection with **Fusion** and **Microsoft Security Copilot**, created production-grade KQL analytics rules, performed threat hunting, automated response with SOAR playbooks, and reduced false positives through tuning. All work mapped to real-world attack simulations using Atomic Red Team.

**Repository Structure**  
- `/KQL-Queries` → Production analytics rules  
- `/Playbooks` → Azure Logic Apps SOAR workflows  
- `/Incident-Reports` → Sample PDF reports with timelines & IOCs  
- `/Screenshots` → Dashboards, alerts & Copilot outputs  
- `/Diagrams` → Architecture & data flow

## Architecture Diagram
```mermaid
graph TD
    A[Data Sources<br/>• Windows Event Logs<br/>• Entra ID Sign-in Logs<br/>• Microsoft Defender for Endpoint<br/>• Azure Activity] 
    --> B[Log Analytics Workspace]
    B --> C[Microsoft Sentinel SIEM]
    C --> D[Fusion AI Engine<br/>Multi-stage attack correlation]
    C --> E[Custom Analytics Rules + KQL Hunting]
    C --> F[Microsoft Security Copilot<br/>Natural-language investigation]
    C --> G[SOAR Playbooks<br/>Azure Logic Apps - Auto-containment]
    G --> H[Automated Actions<br/>• Isolate Host<br/>• Block IP<br/>• Notify Teams]
