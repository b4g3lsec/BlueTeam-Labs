# BlueTeam-Labs
analysis/findings/IRs



## 🕸️ Infrastructure Overview

The lab is structured as an attack-defence sandbox.

| **Node** | **Role** | **Description** |
| ---- | ---- | ----------- |
| Victim | The Target | This is the primary source of telemetry sent to the SIEM. |
| Attacker | Threat Actor | Host running a VM for offensive testing. | 
| SIEM  | Central Log Management | Collects, analyzes and alerts on data received from the sensors. |
| Management | The SOC Station | Primary interface for analysis. Used to manage all nodes via ssh and data visualization via SIEM Dashboard |

## 🛠️ Technology Stack

### Operating Systems
- Victim: Ubuntu Server 24.04.4 LTS
- Attacker: Arch Linux (Host) / Kali Linux (VM)
- Management: MacOS

### Security & Monitoring
- SIEM / XDR: Wazuh Stack (Centralized Manager & Indexer)
- Endpoint sensor: Wazuh Agent (Deployed on the Victim)
- Network IDS/IPS: Snort (Traffic Analysis and Alerting)
- Container: Docker Compose (Managing the Wazuh stack)
- Remote Access: OpenSSH (Access to the nodes with key based authentication only)

### Offensive tools
...


### Repository File Structure

<pre>
.
├── infrastructure/
│   ├── wazuh/
│   │   ├── docker-composer.yaml 
│   │   └── ... 
│   └── snort/
│       ├── rules/
│       └── ...
├── investigations/
│   ├── Phishing-Analysis/
│   │   ├── IR-20260324-WhatsApp-AitM
│   │   │   ├── README.md
│   │   │   └── images/ 
│   │   └── ... 
│   └── ...
├── simulations/
│   └── example-test.md 
└── README.md
</pre>


> [!WARNING]
>
> The content in this repository is for educational and security research purposes only. All analysis was performed on publicly accessible infrastructure or within controlled lab environments.
>
> This research is primarily intended to improve my own understanding of defense tactics and OPSEC.
