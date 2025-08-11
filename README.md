# CST8919 – DevOps Security and Compliance: Cloud Service Alternatives Report

## 1. Find the AWS & GCP Equivalents
Now that I've listed the Azure services from the course, I went ahead and found the closest matching services in AWS and GCP. I focused on how they handle similar tasks like managing identities, monitoring data, enforcing policies, securing postures, and running SIEM operations, pulling from official docs and some online comparison guides to make sure they fit well.

For Azure Active Directory, AWS uses IAM combined with Cognito for access and authentication, while GCP relies on IAM with Cloud Identity for workforce management. Azure Monitor & Log Analytics aligns with AWS CloudWatch for metrics and logs, and GCP's Operations Suite for monitoring. Azure Policy is similar to AWS Organizations with Config for governance, and GCP's Organization Policy Service for constraints. Defender for Cloud matches AWS Security Hub, plus GuardDuty and Inspector for threat and vulnerability scanning, and GCP's Security Command Center for posture. Finally, Azure Sentinel corresponds to AWS GuardDuty with Security Hub and Lambda for detection and automation, and GCP's Chronicle with Security Command Center for SIEM analytics.

## 2. Compare the Services
In this part, I'll compare each Azure service to its AWS and GCP equivalents using straightforward tables. Each table covers a quick overview, core features, security and compliance aspects, pricing, and how they integrate with DevSecOps, based on course emphasis on things like threat detection in logs or automated responses in scenarios.

The comparisons show where Azure often feels more unified, especially for hybrid setups like in the SecureCorp case, while AWS tends to be more modular and scalable, and GCP leans into AI-driven tools. I kept the tables simple for easy reading, highlighting key similarities and differences without going overboard.

### Azure Active Directory (SSO, IAM)
| Aspect | Azure AD | AWS (IAM + Cognito) | GCP (IAM + Cloud Identity) |
|--------|----------|----------------------|-----------------------------|
| Overview | IAM for SSO/MFA/RBAC, hybrid. | Permissions + user auth. | Workforce federation. |
| Core Features | Conditional access, SAML. | Policies, user pools. | SSO, groups. |
| Security & Compliance | ISO/GDPR, Defender threats. | SOC 2, Audit Manager. | ISO/GDPR, Security Center. |
| Pricing | Free basic; $6-9/user/mo. | Free IAM; $0.0055/MAU. | Free; $6/user/mo premium. |
| DevSecOps | DevOps RBAC in pipelines. | CodePipeline access. | Cloud Build identity. |

### Azure Monitor & Log Analytics
| Aspect | Azure Monitor | AWS (CloudWatch) | GCP (Operations Suite) |
|--------|---------------|------------------|------------------------|
| Overview | Telemetry, KQL logs. | Metrics/alarms, logs. | AI logging/monitoring. |
| Core Features | Metrics/traces, alerts. | Alarms, filtering. | Traces, explorer. |
| Security & Compliance | ISO/GDPR, Defender. | SOC 2, Config. | ISO/GDPR, Audit. |
| Pricing | $2.30/GB logs. | $0.30/metric + $0.50/GB. | $0.50/GB. |
| DevSecOps | DevOps logs, alerts. | CodeBuild monitoring. | Cloud Build anomalies. |

### Azure Policy
| Aspect | Azure Policy | AWS (Organizations + Config) | GCP (Organization Policy) |
|--------|--------------|------------------------------|---------------------------|
| Overview | Rule enforcement for compliance. | Account restrictions + monitoring. | Org constraints. |
| Core Features | Initiatives, deny/audit. | SCPs, evaluations. | Boolean policies. |
| Security & Compliance | CIS/GDPR, CSPM. | ISO, Well-Architected. | ISO/GDPR. |
| Pricing | Free. | $0.001/rule. | Free basics. |
| DevSecOps | Blueprints in CI/CD. | CodeCommit governance. | Cloud Source constraints. |

### Defender for Cloud
| Aspect | Defender for Cloud | AWS (Security Hub + GuardDuty/Inspector) | GCP (Security Command Center) |
|--------|--------------------|-----------------------------------------|--------------------------------|
| Overview | CNAPP for posture/threats. | Findings + scans. | Asset threats. |
| Core Features | Score, IaC scans. | Alerts, assessments. | Aggregation, AI. |
| Security & Compliance | ISO/NIST, scans. | SOC 2/CIS. | ISO/GDPR, reports. |
| Pricing | Free base; $0.02/GB. | $0.0012/finding. | Per asset. |
| DevSecOps | GitHub scans. | CodePipeline vulns. | Scanner in builds. |

### Azure Sentinel (SIEM/SOAR)
| Aspect | Azure Sentinel | AWS (GuardDuty + Security Hub/Lambda) | GCP (Chronicle + Security Command Center) |
|--------|----------------|---------------------------------------|-------------------------------------------|
| Overview | SIEM/SOAR with AI. | Detection + automation. | Scalable SIEM. |
| Core Features | KQL, playbooks. | Alerts, workflows. | Analytics, detections. |
| Security & Compliance | GDPR/ISO. | SOC 2/HIPAA. | ISO/GDPR. |
| Pricing | $2.60/GB/mo. | $4/GB. | Per GB. |
| DevSecOps | Logic Apps SOAR. | Step Functions. | Eventarc security. |

## Comparison Table
| Azure Service | AWS Equivalent | GCP Equivalent | Key Diff | Security Edge | Pricing Note | DevSecOps Fit |
|---------------|----------------|-----------------|----------|---------------|--------------|---------------|
| AD | IAM + Cognito | IAM + Cloud ID | Hybrid | Defender | Tiered | RBAC pipes |
| Monitor | CloudWatch | Ops Suite | KQL | Posture | GB | Log alerts |
| Policy | Org + Config | Org Policy | Rules | CSPM | Free | Governance |
| Defender | Hub + GuardDuty | Sec Command | CNAPP | AI | Tiered | IaC |
| Sentinel | GuardDuty + Hub | Chronicle | SOAR | Analytics | GB | Playbooks |

## Narrative Analysis
Azure integrates for DevSecOps (PDF scenarios), AWS modular, GCP AI. Choice by ecosystem.
