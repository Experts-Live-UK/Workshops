### **📌 Zero Trust & Endpoint Security Workshop – Hands-on Lab**  

🚀 **Welcome to the Zero Trust & Endpoint Security Workshop Lab!** 🚀  

This **hands-on lab** is designed to help you follow along with the **workshop session** and re-use the materials for future reference. Throughout this guide, we will walk through **Zero Trust principles, Microsoft Defender for Endpoint (MDE) onboarding, security baselines, and policy management using Intune.**  

---

## **📅 Workshop Details**  
- **Estimated Duration:** ⏱️ **1 hour**  
- **Format:** Hands-on lab using **Microsoft 365 security tools**  
- **Goal:** Equip attendees with **practical skills** to implement Zero Trust security, onboard devices, manage security baselines, and leverage Microsoft Defender for Endpoint effectively.  

---

## **⚡ Prerequisites**  

Before attending the workshop, ensure you have the following:  

✅ **A Microsoft 365 Tenant**  
- You will need an **active Microsoft 365 tenant** with the necessary security and management services enabled.  

✅ **Licenses for Microsoft Defender for Endpoint (MDE) & Intune**  
- Ensure your tenant includes either **Microsoft Defender for Endpoint Plan 1 or Plan 2 (Enterprise or Business)**.  
- **Intune licensing** is required for managing device security policies.  

✅ **Global Administrator Role**  
- You will need **Global Admin** permissions to configure security settings, onboard devices, and manage policies.  

✅ **PowerShell 7 Installed**  
- PowerShell 7 is required for executing scripts used in Intune and Defender for Endpoint onboarding.  
- **[Download PowerShell 7](https://github.com/PowerShell/PowerShell/releases/latest)** if you haven't already installed it.  

# Zero Trust & Endpoint Security Workshop – Hands-on Lab

This repository provides step-by-step guidance for the **Zero Trust & Endpoint Security Workshop**. Attendees can follow along, perform hands-on exercises, and revisit these materials for future reference.

---

## 1️⃣ Zero Trust with Microsoft  

### What is Zero Trust?  
Zero Trust is Microsoft’s security model that assumes **breach by default** and enforces **explicit verification** for every access request. Instead of relying on traditional perimeter-based security, Zero Trust:  

- **Verifies explicitly** – Authenticates users, devices, and apps based on all available data points.  
- **Uses least privilege access** – Grants users only the minimum access needed to perform their roles.  
- **Assumes breach** – Continuously monitors for threats and enforces real-time security responses.  

Microsoft implements Zero Trust through **Entra ID (formerly Azure AD), Intune, Defender for Endpoint, and Microsoft Sentinel**, ensuring **identity, device, and app security** across the enterprise.

---

## 2️⃣ Zero Trust Readiness Assessment  

Microsoft provides a **Zero Trust Readiness Assessment** tool to help organisations evaluate their Zero Trust maturity. The assessment analyzes your **identity, devices, network, applications, data, and security operations** to provide recommendations.

### How to Use the Assessment:  
1. Navigate to **[Zero Trust Readiness Assessment](https://microsoft.github.io/zerotrustassessment/docs/app-permissions)**.  
2. Sign in with your **Microsoft 365 Global Admin** account.  
3. Grant the necessary app permissions.  
4. Run the assessment and review recommendations.  
5. Apply recommended security configurations in **Microsoft Intune, Defender, and Entra ID**.

---

## 3️⃣ Enterprise Access Model & Privileged Access Strategy  

The **Enterprise Access Model (EAM)** is Microsoft’s **modern approach to privileged access management**, ensuring administrators follow strict security practices.  

### Key Privileged Access Tiers:  
1. **Enterprise Security** – Baseline security for standard IT admins with MFA and Conditional Access.  
2. **Specialized Security** – Advanced protections for high-risk accounts, enforcing **Privileged Access Workstations (PAWs)**.  
3. **Privileged Security** – Maximum security for **Tier 0 identities**, requiring **Just-in-Time (JIT) access** and continuous monitoring.

The EAM aligns with **Zero Trust principles**, ensuring privileged users operate under **least privilege and risk-based access controls**.

---

## 4️⃣ Intune Management Tool  

**Intune Manager** is an open-source tool that simplifies policy management in Microsoft Intune. It helps organisations:  
- **Backup configurations** – Export Intune policies for disaster recovery.  
- **Version control policies** – Track and manage policy changes over time.  
- **Deploy and replicate policies** – Import/export settings across multiple tenants.  
- **Document policies** – Maintain records of compliance and security baselines.

More details: **[Intune Manager GitHub Repository](https://github.com/Micke-K/IntuneManagement)**.

---

## 5️⃣ Using Intune Manager  

### How to Use Intune Manager:  
1. Download the latest **Intune Manager** release from [GitHub](https://github.com/Micke-K/IntuneManagement).  
2. Install and run the tool.  
3. Connect to your **Microsoft Intune environment** using your admin credentials.  
4. Select **Export** to back up existing policies or **Import** to deploy new configurations.  
5. Review the applied changes and ensure compliance with your security standards.

---

## 6️⃣ Security Baselines for Intune  

Security baselines in Intune provide **pre-configured security settings** to enforce compliance across Windows devices.  

### Available Security Baselines:  
1. **Native Intune Baselines** – Microsoft provides built-in baselines aligned with Windows security best practices.  
2. **Community Security Baselines** – Open-source baseline templates, such as those from the **Open Intune Baseline Project**.

---

## 7️⃣ Community Security Baselines  

For this workshop, we will use **community-provided baselines** to quickly apply **secure configurations**.  

🔗 **Baseline Repository:** [Open Intune Baseline](https://github.com/SkipToTheEndpoint/OpenIntuneBaseline).  

---

## 8️⃣ Introduction to Microsoft Defender for Endpoint  

**Microsoft Defender for Endpoint (MDE)** is a comprehensive **endpoint detection and response (EDR) solution** that helps organisations:  
- Detect and respond to advanced threats.  
- Manage endpoint vulnerabilities.  
- Automate security investigations and response actions.  
- Integrate security alerts with **Microsoft Sentinel** and **Microsoft 365 Defender**.

---

## 9️⃣ Onboarding to Microsoft Defender for Endpoint with Intune  

To onboard devices to **Defender for Endpoint**, follow these steps:

1. Go to **Microsoft Intune Admin Center** > **Endpoint Security** > **Microsoft Defender for Endpoint**.  
2. Select **Onboarding** and choose the appropriate method (e.g., Intune).  
3. Deploy the **onboarding profile** to target devices.  
4. Verify successful onboarding in the **Microsoft Defender portal**.

---

## 🔟 Post-Onboarding Tasks & Common Mistakes  

After onboarding, complete these **post-deployment steps**:

✅ **Ensure all devices report correctly in the Defender portal**.  
✅ **Check device compliance policies in Intune**.  
✅ **Enable automated investigation and response**.  
✅ **Review common onboarding issues, such as missing Defender agents or misconfigured policies**.

---

## 1️⃣1️⃣ Validating MDE Deployment  

Use these **testing tools** to verify your **Defender for Endpoint** setup:

- **[Defender Testground](https://demo.wd.microsoft.com/)** – Simulate malware detections and endpoint threats.  
- **[MDETester](https://github.com/LearningKijo/MDEtester)** – Run scripted validation tests to check **onboarding success and policy enforcement**.

---

## 1️⃣2️⃣ Proactive Hunting & Incident Response in MDE  

Microsoft Defender for Endpoint provides **advanced security hunting** and **incident response** capabilities:

- **Threat Hunting** – Use **Microsoft 365 Defender Advanced Hunting (KQL queries)** to investigate security anomalies.  
- **Incident Response** – Automate security actions like **isolating compromised devices, blocking malicious files, and triggering remediation workflows**.  
- **Unified SecOps Portal** – Provides a **centralized security dashboard** for monitoring endpoint security.

---

## 1️⃣3️⃣ **DEMO: Using the Unified SecOps Portal**  

_(Follow workshop instructions for the live demo walkthrough.)_  

---

This GitHub guide serves as a reference for the **Zero Trust & Endpoint Security Workshop**, enabling attendees to apply security best practices **beyond the session**.  

🚀 **Ready to secure your environment? Let’s get started!** 🚀  
