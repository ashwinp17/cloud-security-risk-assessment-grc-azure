# Cloud Security Risk Assessment & GRC Simulation — Microsoft Azure

## Project Overview

Conducted a cloud security risk assessment and Governance, Risk, and Compliance simulation against a Microsoft Azure-hosted Windows Server 2022 virtual machine in a controlled lab environment.

The assessment focused on identifying assets, evaluating realistic threat scenarios, identifying security weaknesses, calculating risk based on likelihood and impact, prioritizing remediation, and mapping recommended controls to recognized cybersecurity frameworks.

No exploitation was performed. The project was designed to demonstrate risk-analysis, security-governance, and control-recommendation skills using an authorized educational environment.

## Objectives

- Identify critical cloud assets and access points
- Evaluate threats and vulnerabilities affecting the Azure environment
- Calculate and prioritize risk using likelihood and impact
- Recommend preventive, detective, and corrective security controls
- Apply least-privilege and identity-security principles
- Map recommended controls to recognized cybersecurity frameworks
- Document findings in a professional risk-assessment report

## Assessment Scope

The assessment included the following components:

- Microsoft Azure subscription
- Azure resource group
- Azure-hosted virtual machine
- Windows Server 2022 Datacenter
- Public IP address
- Remote Desktop Protocol access
- Azure Network Security Group rules
- Privileged local administrator account
- Windows Security Event Logs
- Azure monitoring and alerting capabilities

## Environment and Technologies

- Microsoft Azure
- Windows Server 2022 Datacenter
- Azure Virtual Machines
- Azure Network Security Groups
- Remote Desktop Protocol
- Windows Security Event Logs
- Identity and access management
- Role-based access control
- Risk registers
- Risk scoring and prioritization
- NIST Cybersecurity Framework
- CIS Controls

## Assessment Methodology

1. Reviewed the Azure environment and documented the systems, identities, network-access points, and security-monitoring capabilities within scope.
2. Identified assets that could affect system confidentiality, integrity, or availability.
3. Connected each asset to a realistic threat scenario and associated vulnerability.
4. Assigned likelihood and impact scores using a five-point scale.
5. Calculated each risk score by multiplying likelihood by impact.
6. Prioritized risks based on their calculated severity and potential business impact.
7. Recommended preventive, detective, and corrective security controls.
8. Mapped selected controls to the NIST Cybersecurity Framework and CIS Controls.
9. Documented the findings and overall security posture in a formal assessment report.

## Risk-Scoring Model

- **Likelihood:** 1–5
- **Impact:** 1–5
- **Risk Score:** Likelihood × Impact
- **Maximum Score:** 25

Higher scores indicate risks requiring greater remediation priority.

## Confirmed Assessment Findings

### 1. Publicly Exposed Remote Desktop Access

Remote Desktop Protocol was accessible through the virtual machine’s public IP address. Public RDP exposure increases the opportunity for automated scanning, password guessing, and brute-force activity.

**Recommended control:** Restrict inbound RDP access through the Azure Network Security Group to trusted source IP addresses only. Where possible, use a secure administrative-access solution instead of exposing RDP directly to the internet.

### 2. Privileged Administrator Account Without MFA

The local administrator account provided full administrative control over the virtual machine, but multifactor authentication was not enabled for privileged access.

**Recommended control:** Require multifactor authentication for all administrative and privileged accounts. Separate routine user activity from administrative activity and regularly review privileged-account access.

### 3. Operating-System Hardening and Patch Risk

The Windows Server environment required a formal hardening and patch-management process to reduce exposure to known vulnerabilities and insecure default configurations.

**Recommended control:** Apply operating-system security updates regularly, establish a patch-management schedule, and compare the system configuration against an approved Windows Server security baseline.

### 4. Concentration of Privileged Access

A single privileged administrator account created a potential privilege-misuse and concentration-of-access risk. Compromise or misuse of that account could affect high-impact Azure and virtual-machine resources.

**Recommended control:** Enforce role-based access control, apply least privilege, limit privileged-role assignments, and conduct periodic access reviews.

### 5. Limited Centralized Monitoring and Alerting

Windows Security Event Logging and basic Azure monitoring were active. However, centralized log collection, enhanced monitoring, and automated security alerts were not configured.

**Recommended control:** Centralize security logs through Azure Monitor or Microsoft Defender for Cloud and configure alerts for suspicious authentication, privilege changes, account-management events, and abnormal system activity.

## Sample Risk Register Findings

| Risk | Likelihood | Impact | Risk Score | Recommended Control |
|---|---:|---:|---:|---|
| Brute-force attack against publicly exposed RDP | 4/5 | 4/5 | 16/25 | Restrict inbound RDP access through the Azure Network Security Group to trusted IP addresses |
| Compromise of the privileged local administrator account¹ | 3/5 | 5/5 | 15/25 | Enforce multifactor authentication for all administrative and privileged accounts |
| Exploitation of Windows Server vulnerabilities | 3/5 | 4/5 | 12/25 | Implement formal patch management and apply operating-system security updates |
| Privilege misuse within the Azure subscription | 2/5 | 5/5 | 10/25 | Enforce role-based access control and least-privilege access |
| Malicious activity remaining undetected because of limited monitoring | 3/5 | 3/5 | 9/25 | Enable centralized logging, enhanced monitoring, and automated security alerts |

¹ *Likelihood was scored moderate at 3/5 because successful compromise would require an attacker to obtain or correctly guess valid administrative credentials, although publicly exposed RDP increases the opportunity for credential-based attacks. Impact was scored maximum at 5/5 because compromise of the account would provide full administrative control over the virtual machine. The resulting score demonstrates how severe potential impact can elevate remediation priority even when likelihood is not rated at its maximum.*

## Security-Control Mapping

| Identified Risk | Recommended Control | Control Type | Framework Mapping |
|---|---|---|---|
| Public RDP exposure | Restrict inbound administrative access to trusted source IP addresses | Preventive | CIS Control 4 |
| Administrative credential compromise | Enforce multifactor authentication | Preventive | NIST CSF 2.0 PR.AA-03 |
| Operating-system vulnerabilities | Establish patch and vulnerability-management procedures | Corrective | CIS Control 7 |
| Privilege misuse | Enforce role-based access control and least privilege | Preventive | CIS Control 5 |
| Limited security monitoring | Centralize logs and configure automated alerts | Detective | NIST CSF DE.CM |

## Prioritized Remediation Plan

### Immediate Priority

- Restrict publicly exposed RDP access
- Enable multifactor authentication for privileged accounts
- Review all administrator and Azure role assignments

### Near-Term Priority

- Apply operating-system patches and security updates
- Establish a hardened Windows Server configuration baseline
- Configure centralized logging and automated security alerts

### Ongoing Priority

- Review privileged access regularly
- Audit Network Security Group rules
- Monitor authentication and account-management activity
- Test incident-response and recovery procedures
- Reassess risks after major configuration changes

## Overall Risk Posture

The assessed environment demonstrated a **medium-to-high risk posture**.

Although the environment was limited to a single Azure virtual machine, publicly exposed RDP increased the attack surface and created an opportunity for automated credential attacks. The privileged administrator account increased the potential impact of credential compromise because it provided full control over the system.

The environment’s risk posture could be significantly improved by restricting remote administrative access, enforcing multifactor authentication, applying least privilege, maintaining operating-system patches, and implementing centralized security monitoring and alerting.

## Skills Demonstrated

- Cloud security risk assessment
- Asset, threat, and vulnerability identification
- Risk-register development
- Qualitative risk scoring
- Risk prioritization
- Security-control selection
- Identity and access-management analysis
- Role-based access-control concepts
- Azure security analysis
- NIST CSF and CIS Controls mapping
- Remediation planning
- Technical and executive report writing

## Full Report

[View the complete Cloud Security Risk Assessment and GRC Report](Cloud_Security_Risk_Assessment_GRC_Report.pdf)

## Assessment Limitations

- The assessment was conducted in a controlled educational lab.
- No exploitation or unauthorized testing was performed.
- Findings were based on the environment and configurations observed during the assessment.
- Recommended controls should be validated against an organization’s operational requirements before production implementation.

## Disclaimer

This project was completed for educational and portfolio purposes using an authorized Microsoft Azure lab environment. No real organizational systems, production resources, or unauthorized cloud assets were assessed.
