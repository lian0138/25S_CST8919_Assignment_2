# CST8919 – DevOps Security and Compliance: Cloud Service Alternatives Report

## 1. Azure Active Directory (SSO, IAM)

Azure Active Directory (Microsoft Entra ID) is a cloud-based identity and access management service providing single sign-on (SSO), multi-factor authentication (MFA), and role-based access control (RBAC) in hybrid environments. The AWS equivalent combines IAM for resource permissions and Cognito for user authentication and sign-on. The GCP equivalent pairs IAM for permissions with Cloud Identity for workforce SSO and federation.

### Comparison Details
- **Core Features**: Azure AD offers conditional access policies, SAML/OpenID support, and self-service password resets; AWS provides fine-grained policies and user pools for authentication; GCP includes group-based access and federation with external identity providers.
- **Security & Compliance**: All services support ISO 27001 and GDPR; Azure integrates with Defender for threat detection, AWS uses Audit Manager for SOC 2/HIPAA compliance, and GCP ties into Security Command Center for monitoring.
- **Pricing Model**: Azure is free for basics with Premium tiers at $6-9/user/month; AWS IAM is free, but Cognito charges $0.0055 per monthly active user (MAU) beyond the free tier; GCP offers a free edition and Premium at $6/user/month, often bundled with Workspace.
- **Integration for DevSecOps**: Azure AD integrates with Azure DevOps and GitHub Actions for automated RBAC in CI/CD pipelines; AWS works with CodePipeline and Lambda for access automation; GCP supports Cloud Build and GitHub for identity management in workflows.

In summary, Azure AD excels in hybrid and enterprise SSO scenarios with strong Defender ties, while AWS offers modular flexibility and GCP emphasizes simplicity; for DevSecOps, Azure's seamless pipeline integration makes it preferable for Microsoft-centric ecosystems, though AWS may be more cost-effective for high-scale user management based on 2024 pricing analyses from Jit.

## 2. Azure Monitor & Log Analytics
Azure Monitor is a comprehensive service for collecting telemetry data, with Log Analytics providing KQL-based querying for logs and insights. The AWS equivalent is CloudWatch, which handles metrics, alarms, and log management. The GCP equivalent is Operations Suite (formerly Stackdriver), offering AI-driven logging, monitoring, and operations.

### Comparison Details
- **Core Features**: Azure provides metrics collection, traces, alerts, and customizable dashboards; AWS includes metric alarms, log insights, and event rules; GCP features log explorer, metrics, traces, and AI-powered anomaly detection.
- **Security & Compliance**: All align with ISO 27001 and GDPR; Azure links to Defender for security posture, AWS integrates with Config for SOC 2/HIPAA, and GCP uses Cloud Audit Logs for tracking.
- **Pricing Model**: Azure charges $2.30/GB for ingested logs with free basic metrics and reservation discounts; AWS is $0.30 per metric/month plus $0.50/GB for logs, with a free tier; GCP is $0.50/GB for logs on a pay-as-you-go basis with free quotas.
- **Integration for DevSecOps**: Azure integrates with Azure DevOps and Logic Apps for CI/CD monitoring and alerts; AWS supports CodeBuild and CodePipeline for automation; GCP works with Cloud Build and Error Reporting for pipeline insights.

In summary, Azure's KQL enables powerful threat analysis, AWS shines in real-time alarms, and GCP leverages AI for insights; Azure's hybrid monitoring and DevSecOps compatibility make it ideal for complex environments, potentially more economical for large logs via reservations as per 2024 Sysdig reports.

## 3. Azure Policy
Azure Policy is a governance tool that enforces and audits compliance rules across cloud resources to prevent misconfigurations. The AWS equivalent combines Organizations with Service Control Policies (SCPs) and Config for account management and rule tracking. The GCP equivalent is Organization Policy Service, which applies constraints across projects and folders.

### Comparison Details
- **Core Features**: Azure includes policy definitions, initiatives, and effects like deny/audit/remediate; AWS offers SCPs for restrictions and Config rules for evaluations; GCP provides boolean constraints with policy inheritance.
- **Security & Compliance**: All support CIS benchmarks, GDPR, and ISO 27001; Azure integrates with Defender for CSPM, AWS follows the Well-Architected Framework, and GCP enforces standards like resource location restrictions.
- **Pricing Model**: Azure is free with minimal costs for resource evaluations; AWS Organizations is free, but Config charges $0.001 per rule evaluation; GCP is free for basic use without additional fees.
- **Integration for DevSecOps**: Azure uses Blueprints and GitHub Actions for policy-as-code in CI/CD; AWS integrates with CodeCommit and CodePipeline for governance; GCP supports Cloud Source Repositories and Cloud Build for automated policy checks.

In summary, Azure provides granular remediation for compliance, AWS emphasizes ongoing monitoring, and GCP offers straightforward org-wide constraints; Azure's no-cost model and strong DevSecOps integration suit governance-heavy setups, as highlighted in 2024 Pluralsight governance comparisons.

## 4. Defender for Cloud
Defender for Cloud is a Cloud-Native Application Protection Platform (CNAPP) focused on security posture management (CSPM), workload protection (CWPP), and DevSecOps. The AWS equivalent is Security Hub combined with GuardDuty for threat detection and Inspector for vulnerability scanning. The GCP equivalent is Security Command Center, which centralizes asset inventory, threats, and posture insights.

### Comparison Details
- **Core Features**: Azure offers secure score, IaC scanning, and AI-driven alerts; AWS provides automated threat findings and vuln assessments; GCP includes findings aggregation and AI insights for vulnerabilities.
- **Security & Compliance**: All meet ISO 27001, NIST, and CIS standards; Azure includes regulatory assessments, AWS supports SOC 2 and multi-account checks, and GCP provides GDPR-compliant reports.
- **Pricing Model**: Azure has free foundational CSPM with enhanced tiers at $0.02/GB or per resource; AWS Security Hub is $0.001 per check, GuardDuty $0.0012/finding; GCP is pay-per-asset/resource with free starters.
- **Integration for DevSecOps**: Azure integrates with GitHub for IaC scans and Azure DevOps for fixes; AWS uses CodePipeline and Lambda for vuln automation; GCP supports Cloud Build and Security Scanner in pipelines.

In summary, Azure's unified multi-cloud CNAPP leads in posture management, AWS in threat intelligence, and GCP in asset-based insights; Azure's tiered pricing and DevSecOps tools make it versatile for hybrids, updated for 2024 compliance from Google Cloud resources.

## 5. Azure Sentinel (SIEM/SOAR)
Azure Sentinel is a cloud-native SIEM and SOAR solution for threat detection, investigation, and automated responses using AI. The AWS equivalent combines GuardDuty for threat detection, Security Hub for aggregation, and Lambda for automation. The GCP equivalent pairs Chronicle for scalable SIEM with Security Command Center for insights.

### Comparison Details
- **Core Features**: Azure includes KQL analytics, hunting queries, and playbooks; AWS offers intelligent alerts and serverless workflows; GCP provides log analytics and AI-driven detections with case management.
- **Security & Compliance**: All comply with GDPR, ISO 27001, and SOC 2; Azure offers data sovereignty, AWS supports HIPAA with audit trails, and GCP ensures data residency.
- **Pricing Model**: Azure is $2.60/GB per month for ingested data with pay-as-you-go tiers; AWS GuardDuty is $4/GB analyzed; GCP Chronicle is per GB ingested, scaling with volume.
- **Integration for DevSecOps**: Azure uses Logic Apps and Azure DevOps for CI/CD incident response; AWS integrates Step Functions with CodePipeline; GCP supports Eventarc and Cloud Build for automated security workflows.

In summary, Azure's integrated SOAR excels in orchestration, AWS in rapid detection, and GCP in big-data scaling; Azure's AI analytics and DevSecOps compatibility provide strong value for automated responses, as noted in 2024 Varonis and Sysdig SIEM comparisons.


## Overall Comparison Table
| Azure Service          | AWS Equivalent                  | GCP Equivalent                  | Key Difference                  | Security Edge                  | Pricing Note                  | DevSecOps Fit                  |
|------------------------|---------------------------------|---------------------------------|---------------------------------|--------------------------------|--------------------------------|--------------------------------|
| Azure AD (SSO, IAM)    | IAM + Cognito                   | IAM + Cloud Identity            | Azure hybrid SSO vs. AWS modular | Azure Defender integration     | Azure tiered ($6-9/user)       | Azure pipeline RBAC            |
| Monitor & Log Analytics| CloudWatch                      | Operations Suite                | Azure KQL depth vs. GCP AI      | Azure posture links            | Azure $2.30/GB ingest          | Azure CI/CD alerts             |
| Azure Policy           | Organizations + Config          | Organization Policy             | Azure remediation vs. AWS rules | Azure CSPM                     | Azure free                     | Azure policy-as-code           |
| Defender for Cloud     | Security Hub + GuardDuty/Inspector | Security Command Center       | Azure CNAPP unity vs. GCP assets| Azure AI scans                 | Azure tiered ($0.02/GB)        | Azure IaC scans                |
| Azure Sentinel (SIEM/SOAR) | GuardDuty + Security Hub/Lambda | Chronicle + Security Command Center | Azure SOAR built-in vs. AWS detection | Azure analytics            | Azure $2.60/GB                 | Azure playbook automation      |

## Narrative Analysis
I think Azure really stands out with its super tight integration and support for hybrid setups, which makes it perfect for stuff like the SecureCorp migration we talked about in class—it's all about having everything work together smoothly in DevSecOps, from handling logins to dealing with threats. AWS is cool for its scalability and how it breaks things down into modules, plus the pricing is based on what you use, so it can save money if you're dealing with tons of data, but you might have to tinker more to get it all flowing nicely. GCP is great if you're into AI and crunching big data with less hassle in setup, though it doesn't have as much built-in automation for responses like Azure does. From what we learned about shared responsibility and tools like KQL for spotting issues, I'd probably pick Azure if you're already in the Microsoft world, but go for AWS if you're watching costs or GCP if AI is your thing—really, it comes down to what ecosystem you're in and your compliance needs, like what I've seen in those Sysdig and Varonis articles from 2024.
