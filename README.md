# CST8919 – DevOps Security and Compliance: Cloud Service Alternatives Report

## Azure Active Directory (SSO, IAM)
### Overview
Azure Active Directory (Microsoft Entra ID) is a cloud-based identity and access management service providing single sign-on (SSO), multi-factor authentication (MFA), and role-based access control (RBAC) in hybrid environments. The AWS equivalent combines IAM for resource permissions and Cognito for user authentication and sign-on. The GCP equivalent pairs IAM for permissions with Cloud Identity for workforce SSO and federation.

### Comparison Details
- **Core Features**: Azure AD offers conditional access policies, SAML/OpenID support, and self-service password resets; AWS provides fine-grained policies and user pools for authentication; GCP includes group-based access and federation with external identity providers.
- **Security & Compliance**: All services support ISO 27001 and GDPR; Azure integrates with Defender for threat detection, AWS uses Audit Manager for SOC 2/HIPAA compliance, and GCP ties into Security Command Center for monitoring.
- **Pricing Model**: Azure is free for basics with Premium tiers at $6-9/user/month; AWS IAM is free, but Cognito charges $0.0055 per monthly active user (MAU) beyond the free tier; GCP offers a free edition and Premium at $6/user/month, often bundled with Workspace.
- **Integration for DevSecOps**: Azure AD integrates with Azure DevOps and GitHub Actions for automated RBAC in CI/CD pipelines; AWS works with CodePipeline and Lambda for access automation; GCP supports Cloud Build and GitHub for identity management in workflows.

### Overall Comparison Table
| Aspect                  | Azure AD               | AWS IAM + Cognito      | GCP IAM + Cloud Identity |
|-------------------------|------------------------|------------------------|--------------------------|
| Core Features           | Conditional access, SAML | Policies, user pools  | SSO, groups              |
| Security & Compliance   | ISO/GDPR, Defender     | SOC 2, Audit Manager   | ISO/GDPR, Security Center|
| Pricing Model           | Free basic; $6-9/user/mo | Free IAM; $0.0055/MAU | Free; $6/user/mo premium |
| Integration for DevSecOps | DevOps RBAC pipelines | CodePipeline access    | Cloud Build identity     |

### Conclution
Azure AD feels like the go-to for handling logins and access in mixed setups, especially with its hybrid support that ties right into stuff like Defender for spotting threats early, just like we talked about in class for SecureCorp. AWS with IAM and Cognito is super flexible if you want to tweak permissions finely, but it might take more setup time, and GCP's IAM plus Cloud Identity keeps things simple for quick workforce access. From a DevSecOps angle, Azure makes automating roles in pipelines a breeze, which saves headaches, though if you're watching pennies for tons of users, AWS could be cheaper—based on what I've seen in 2024 Jit reports, I'd pick Azure unless you're all-in on Google tools.

## Azure Monitor & Log Analytics
### Overview
Azure Monitor is a comprehensive service for collecting telemetry data, with Log Analytics providing KQL-based querying for logs and insights. The AWS equivalent is CloudWatch, which handles metrics, alarms, and log management. The GCP equivalent is Operations Suite (formerly Stackdriver), offering AI-driven logging, monitoring, and operations.

### Comparison Details
- **Core Features**: Azure provides metrics collection, traces, alerts, and customizable dashboards; AWS includes metric alarms, log insights, and event rules; GCP features log explorer, metrics, traces, and AI-powered anomaly detection.
- **Security & Compliance**: All align with ISO 27001 and GDPR; Azure links to Defender for security posture, AWS integrates with Config for SOC 2/HIPAA, and GCP uses Cloud Audit Logs for tracking.
- **Pricing Model**: Azure charges $2.30/GB for ingested logs with free basic metrics and reservation discounts; AWS is $0.30 per metric/month plus $0.50/GB for logs, with a free tier; GCP is $0.50/GB for logs on a pay-as-you-go basis with free quotas.
- **Integration for DevSecOps**: Azure integrates with Azure DevOps and Logic Apps for CI/CD monitoring and alerts; AWS supports CodeBuild and CodePipeline for automation; GCP works with Cloud Build and Error Reporting for pipeline insights.

### Overall Comparison Table
| Aspect                  | Azure Monitor          | AWS CloudWatch         | GCP Operations Suite   |
|-------------------------|------------------------|------------------------|------------------------|
| Core Features           | Metrics/traces, alerts | Alarms, filtering      | Traces, explorer       |
| Security & Compliance   | ISO/GDPR, Defender     | SOC 2, Config          | ISO/GDPR, Audit        |
| Pricing Model           | $2.30/GB logs          | $0.30/metric + $0.50/GB| $0.50/GB               |
| Integration for DevSecOps | DevOps logs, alerts   | CodeBuild monitoring   | Cloud Build anomalies   |

### Conclution
With Azure Monitor and Log Analytics, it's like having a sharp tool for digging into logs with KQL, which we used in class for spotting issues fast, and it plays nice with Defender for that extra security layer. AWS CloudWatch is reliable for quick alarms and metrics, but feels a bit more basic unless you add extras, while GCP's Operations Suite brings in cool AI to catch weird patterns automatically. For DevSecOps, Azure fits right into your pipelines for real-time checks, making life easier, though GCP might edge out if you're into AI-driven stuff— from those 2024 Sysdig breakdowns, Azure's probably your best bet for hybrid monitoring without breaking the bank on big data.

## Azure Policy
### Overview
Azure Policy is a governance tool that enforces and audits compliance rules across cloud resources to prevent misconfigurations. The AWS equivalent combines Organizations with Service Control Policies (SCPs) and Config for account management and rule tracking. The GCP equivalent is Organization Policy Service, which applies constraints across projects and folders.

### Comparison Details
- **Core Features**: Azure includes policy definitions, initiatives, and effects like deny/audit/remediate; AWS offers SCPs for restrictions and Config rules for evaluations; GCP provides boolean constraints with policy inheritance.
- **Security & Compliance**: All support CIS benchmarks, GDPR, and ISO 27001; Azure integrates with Defender for CSPM, AWS follows the Well-Architected Framework, and GCP enforces standards like resource location restrictions.
- **Pricing Model**: Azure is free with minimal costs for resource evaluations; AWS Organizations is free, but Config charges $0.001 per rule evaluation; GCP is free for basic use without additional fees.
- **Integration for DevSecOps**: Azure uses Blueprints and GitHub Actions for policy-as-code in CI/CD; AWS integrates with CodeCommit and CodePipeline for governance; GCP supports Cloud Source Repositories and Cloud Build for automated policy checks.

### Overall Comparison Table
| Aspect                  | Azure Policy           | AWS Organizations + Config | GCP Organization Policy |
|-------------------------|------------------------|----------------------------|-------------------------|
| Core Features           | Initiatives, deny/audit| SCPs, evaluations          | Boolean policies        |
| Security & Compliance   | CIS/GDPR, CSPM         | ISO, Well-Architected      | ISO/GDPR                |
| Pricing Model           | Free                   | $0.001/rule                | Free basics             |
| Integration for DevSecOps | Blueprints in CI/CD   | CodeCommit governance      | Cloud Source constraints|

### Conclution
Azure Policy is straightforward for keeping things compliant, like enforcing rules in landing zones as per our class slides, and it hooks up with Defender to catch posture issues early. AWS's combo of Organizations and Config gives you solid monitoring and restrictions, but you pay per rule which adds up, and GCP's Organization Policy is simple for quick constraints across teams. In DevSecOps, Azure lets you bake policies into CI/CD easily, which is a time-saver, though AWS might appeal if you need detailed evals—from 2024 Pluralsight notes, Azure's free tier makes it practical for most setups unless you want GCP's no-fuss approach.

## Defender for Cloud
### Overview
Defender for Cloud is a Cloud-Native Application Protection Platform (CNAPP) focused on security posture management (CSPM), workload protection (CWPP), and DevSecOps. The AWS equivalent is Security Hub combined with GuardDuty for threat detection and Inspector for vulnerability scanning. The GCP equivalent is Security Command Center, which centralizes asset inventory, threats, and posture insights.

### Comparison Details
- **Core Features**: Azure offers secure score, IaC scanning, and AI-driven alerts; AWS provides automated threat findings and vuln assessments; GCP includes findings aggregation and AI insights for vulnerabilities.
- **Security & Compliance**: All meet ISO 27001, NIST, and CIS standards; Azure includes regulatory assessments, AWS supports SOC 2 and multi-account checks, and GCP provides GDPR-compliant reports.
- **Pricing Model**: Azure has free foundational CSPM with enhanced tiers at $0.02/GB or per resource; AWS Security Hub is $0.001 per check, GuardDuty $0.0012/finding; GCP is pay-per-asset/resource with free starters.
- **Integration for DevSecOps**: Azure integrates with GitHub for IaC scans and Azure DevOps for fixes; AWS uses CodePipeline and Lambda for vuln automation; GCP supports Cloud Build and Security Scanner in pipelines.

### Overall Comparison Table
| Aspect                  | Defender for Cloud     | AWS Security Hub + GuardDuty/Inspector | GCP Security Command Center |
|-------------------------|------------------------|---------------------------------------|-----------------------------|
| Core Features           | Score, IaC scans       | Alerts, assessments                   | Aggregation, AI             |
| Security & Compliance   | ISO/NIST, scans        | SOC 2/CIS                             | ISO/GDPR, reports           |
| Pricing Model           | Free base; $0.02/GB    | $0.0012/finding                       | Per asset                   |
| Integration for DevSecOps | GitHub scans          | CodePipeline vulns                    | Scanner in builds           |

### Conclution
Defender for Cloud pulls everything together as a CNAPP, giving you scores and scans that fit right into DevSecOps like checking IaC in GitHub, which lines up with class talks on protecting workloads. AWS's mix of Security Hub, GuardDuty, and Inspector is great for piecing together threats and vulns, but it's more modular so setup takes effort, and GCP's Security Command Center is handy for quick asset overviews with AI help. For serverless security, Azure's unified vibe makes it less of a hassle, especially with free basics, though AWS could be better for detailed findings—per 2024 Google Cloud updates, Azure works well in hybrids without overwhelming costs.

## Azure Sentinel (SIEM/SOAR)
### Overview
Azure Sentinel is a cloud-native SIEM and SOAR solution for threat detection, investigation, and automated responses using AI. The AWS equivalent combines GuardDuty for threat detection, Security Hub for aggregation, and Lambda for automation. The GCP equivalent pairs Chronicle for scalable SIEM with Security Command Center for insights.

### Comparison Details
- **Core Features**: Azure includes KQL analytics, hunting queries, and playbooks; AWS offers intelligent alerts and serverless workflows; GCP provides log analytics and AI-driven detections with case management.
- **Security & Compliance**: All comply with GDPR, ISO 27001, and SOC 2; Azure offers data sovereignty, AWS supports HIPAA with audit trails, and GCP ensures data residency.
- **Pricing Model**: Azure is $2.60/GB per month for ingested data with pay-as-you-go tiers; AWS GuardDuty is $4/GB analyzed; GCP Chronicle is per GB ingested, scaling with volume.
- **Integration for DevSecOps**: Azure uses Logic Apps and Azure DevOps for CI/CD incident response; AWS integrates Step Functions with CodePipeline; GCP supports Eventarc and Cloud Build for automated security workflows.

### Overall Comparison Table
| Aspect                  | Azure Sentinel         | AWS GuardDuty + Security Hub/Lambda | GCP Chronicle + Security Command Center |
|-------------------------|------------------------|-------------------------------------|-----------------------------------------|
| Core Features           | KQL, playbooks         | Alerts, workflows                   | Analytics, detections                    |
| Security & Compliance   | GDPR/ISO               | SOC 2/HIPAA                         | ISO/GDPR                                |
| Pricing Model           | $2.60/GB/mo            | $4/GB                               | Per GB                                  |
| Integration for DevSecOps | Logic Apps SOAR       | Step Functions                      | Eventarc security                       |

### Conclution
Azure Sentinel is pretty slick for SIEM with its KQL queries and playbooks that automate responses, like the SOAR stuff we covered in class for handling incidents without manual fuss. AWS's GuardDuty, Security Hub, and Lambda combo gets you solid detection and workflows, but it's piecemeal so you build more yourself, and GCP's Chronicle with Security Center scales for huge logs with AI smarts. In DevSecOps, Azure plugs into pipelines for quick incident handling, which is a win, though GCP might be better for massive data— from 2024 Varonis and Sysdig pieces, Azure feels right for most if you want that integrated automation without extra hassle.
```
