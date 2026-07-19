# Cloud Security Risk Assessment & GRC Simulation (Azure)

## Project Overview

Conducted a cloud security risk assessment and Governance, Risk, and Compliance simulation using an Azure-based business scenario.

The project involved identifying cloud security risks, evaluating their likelihood and business impact, prioritizing the risks, and recommending appropriate security controls and remediation strategies.

> This project was completed in a controlled educational environment. No real organizational systems or unauthorized cloud resources were assessed.

## Objectives

- Identify cloud security threats and vulnerabilities
- Evaluate risks based on likelihood and business impact
- Prioritize risks according to severity
- Recommend administrative and technical security controls
- Apply Governance, Risk, and Compliance concepts
- Document findings in a professional risk assessment report

## Environment and Technologies

- Microsoft Azure
- Cloud security
- Governance, Risk, and Compliance
- Risk assessment and risk management
- Risk registers
- Identity and access management
- Business continuity and disaster recovery
- Security control recommendations

## Assessment Process

1. Reviewed the Azure-based business scenario
2. Identified threats, vulnerabilities, and affected assets
3. Evaluated the likelihood and potential impact of each risk
4. Assigned risk levels and priorities
5. Recommended security controls
6. Developed remediation strategies
7. Documented the final findings

## Sample Risk Register Findings

| Risk | Likelihood | Impact | Risk Score | Recommended Control |
|---|---:|---:|---:|---|
| Brute-force attack against publicly exposed RDP | 4/5 | 4/5 | 16/25 | Restrict inbound RDP access through the Azure Network Security Group to trusted IP addresses only |
| Compromise of the privileged local administrator account¹ | 3/5 | 5/5 | 15/25 | Enforce multifactor authentication for all administrative and privileged accounts |
| Exploitation of unpatched Windows Server vulnerabilities | 3/5 | 4/5 | 12/25 | Implement regular patch management and apply operating-system security updates |
| Privilege misuse within the Azure subscription | 2/5 | 5/5 | 10/25 | Enforce role-based access control and least-privilege access for Azure resources |
| Malicious activity remaining undetected due to limited monitoring | 3/5 | 3/5 | 9/25 | Enable centralized logging and security alerts through Azure Monitor or Microsoft Defender for Cloud |

¹ *Likelihood was scored moderate (3/5) because account compromise would require an attacker to obtain or successfully guess valid administrative credentials, although publicly exposed RDP increases the opportunity for credential-based attacks. Impact was scored maximum (5/5) because compromise of this account would provide full control over the virtual machine — illustrating how high potential impact can elevate remediation priority even when likelihood isn't at the maximum level.*

## Key Risk Areas

- Identity and access management
- Excessive permissions
- Data exposure
- Cloud misconfiguration
- Insufficient monitoring and logging
- Business continuity
- Disaster recovery
- Policy and regulatory compliance

## Sample Risk Register Findings

| Risk | Likelihood | Impact | Risk Score | Recommended Control |
|---|---:|---:|---:|---|
| Brute-force attack against publicly exposed RDP | 4/5 | 4/5 | 16/25 | Restrict inbound RDP access through the Azure Network Security Group to trusted IP addresses only |
| Compromise of the privileged local administrator account | 3/5 | 5/5 | 15/25 | Enforce multifactor authentication for all administrative and privileged accounts |
| Exploitation of unpatched Windows Server vulnerabilities | 3/5 | 4/5 | 12/25 | Implement regular patch management and apply operating-system security updates |
| Privilege misuse within the Azure subscription | 2/5 | 5/5 | 10/25 | Enforce role-based access control and least-privilege access for Azure resources |
| Malicious activity remaining undetected due to limited monitoring | 3/5 | 3/5 | 9/25 | Enable centralized logging and security alerts through Azure Monitor or Microsoft Defender for Cloud |

## Skills Demonstrated

- Cloud security risk analysis
- Risk identification and prioritization
- Governance, Risk, and Compliance
- Risk-register development
- Security-control selection
- Azure security concepts
- Business-impact analysis
- Remediation planning
- Technical report writing

## Full Report

[View the complete Cloud Security Risk Assessment and GRC Report](Cloud_Security_Risk_Assessment_GRC_Report.pdf)

## Disclaimer

This project was completed for educational and portfolio purposes using a controlled Azure-based scenario. No real organizational systems or unauthorized cloud resources were tested.
