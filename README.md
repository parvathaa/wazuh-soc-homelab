Wazuh SOC Homelab

A personal Security Operations Center (SOC) homelab built using Wazuh SIEM/XDR to gain hands-on experience with endpoint monitoring, threat detection, log analysis, and MITRE ATT&CK mapping.

Project Objectives
Deploy a production-style SIEM environment
Monitor endpoints using Wazuh agents
Generate security events through attack simulation
Investigate alerts using Threat Hunting
Map detections to the MITRE ATT&CK framework
Develop practical SOC analyst skills
Environment
Component	Description
SIEM	Wazuh 4.14.5
Manager OS	Ubuntu 24 LTS
Agent OS	macOS Apple Silicon
Firewall	UFW
Attack Vector	SSH Brute Force
Framework	MITRE ATT&CK
Architecture

Network Layout
Role	Host
Wazuh Manager	Ubuntu 24
Wazuh Agent	MacBook Air M1
Phase 1 – Wazuh Deployment
Tasks Completed
Installed Wazuh Manager on Ubuntu
Configured HTTPS dashboard
Configured UFW firewall
Installed Wazuh Agent on macOS
Registered endpoint with manager
Verified telemetry collection
Agent Status

Phase 2 – Attack Simulation
SSH Brute Force

A simulated brute-force attack was launched from the macOS endpoint against the Ubuntu host.

for i in {1..10}; do
ssh wronguser@10.135.235.2
done

Detection Results

Wazuh successfully detected and classified the attack.

Alerts Triggered
Rule ID	Description	MITRE
5710	Invalid user login attempt	T1110
5503	PAM authentication failure	T1110
2502	Multiple failed passwords	T1110
Threat Hunting Dashboard

MITRE ATT&CK Mapping

The generated events were automatically mapped by Wazuh to MITRE ATT&CK techniques.

Observed Techniques
Technique	Description
T1110	Brute Force
T1078	Valid Accounts
T1548	Abuse Elevation Control Mechanism

Skills Demonstrated
SIEM Deployment
Endpoint Monitoring
Threat Detection
Log Analysis
Alert Investigation
MITRE ATT&CK Mapping
Linux Administration
Firewall Configuration
Security Monitoring
Blue Team Operations
Key Takeaways

This project demonstrates the complete detection lifecycle:

Deploy monitoring infrastructure
Generate attack activity
Collect telemetry
Detect malicious behavior
Investigate alerts
Map activity to ATT&CK techniques
Future Improvements
Integrate Suricata IDS
Add VirusTotal integration
Create custom Wazuh detection rules
Add Sigma rule testing
Monitor Windows endpoints
Build automated incident response workflows
Author

Parvatha

MSc Cybersecurity — University of Manchester

SOC Analyst | Cloud Security Enthusiast
