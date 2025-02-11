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
- PowerShell 7 is required for executing some of the community tools used throughout the workshop.  
- **[Download PowerShell 7](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.5)** if you haven't already installed it.  

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
2. Open PowerShell 7 on your device, and install the module following the steps provided in the link.   
3. Run the assessment and review recommendations.

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
2. Extract the downloadeded zip file.
3. Unblock all .cmd and .ps/psm/psd files - **You can do this by right clicking the file and selecting the Unblock checkbox**
4. ![image](https://github.com/user-attachments/assets/38f6e683-1590-4edd-8c90-16ab3503fb29)
5. Open PowerShell 7 and navigate to the folder - **Example: cd C:\Temp\IntuneManagement-master**
6. ![image](https://github.com/user-attachments/assets/1d96a337-dccd-4b6b-a800-b95a7c0fe4ea)
7. Run the tool by typing **.\start-Intunemanagement.ps1**
8. ![image](https://github.com/user-attachments/assets/56e371c5-8883-4d04-b2b6-4eb72b074acb)
9. Using the profile icon in the top right, sign in using your global admin account
10. ![image](https://github.com/user-attachments/assets/f8135ab2-58fd-4f97-94cd-c64bab7c19c4)
11. Accept any graph permissions required.
12. ![image](https://github.com/user-attachments/assets/75e0eec3-416d-431d-a11d-30138ca263f8)
13. Select the profile icon again, and choose request consent, approve these again.
14. ![image](https://github.com/user-attachments/assets/81b7e385-712f-4fff-b021-6dd4031daefa)
15. ![image](https://github.com/user-attachments/assets/5b2dc3de-fd58-46ff-8242-b9b0c78bd973)
16. From here you can select the required module and export/import or document policy configurations.

If you have any issues you can use the following guide: https://www.natehutchinson.co.uk/post/easily-import-export-and-document-intune-configurations 

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

### Import the required policies using the Intune Management tool
![image](https://github.com/user-attachments/assets/d6d2aeeb-7964-4ed5-9e45-cdf7bbee4c90)


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

1. Go to **Microsoft Defender Portal** (https://security.microsoft.com) > **Settings** > **Endpoints** > **Advanced Features** > **Microsoft Intune**
2. Enable the toggle for the **Microsoft Intune** connection.
3. ![image](https://github.com/user-attachments/assets/98a67b38-b1fd-4df7-9761-60603048a9de)
4. Go to **Microsoft Intune Portal** > **Tenant Administration** > **Connectors and Tokens** > **Microsoft Defender for Endpoint**
5. Confirm **Connection status** is **Enabled** and switch all platform compliance policy evaluation settings to **On**
6. ![image](https://github.com/user-attachments/assets/fe06178f-477b-4489-a16f-3d530f88316f)
7. Go to **Endpoint Security** node in Intune > **Endpoint detection and response** and create a new policy with the below settings.
8. ![image](https://github.com/user-attachments/assets/abce36ed-eb2e-4357-8fa1-803a8cfe70d2)
9. ![image](https://github.com/user-attachments/assets/0dcd8e11-8e08-4ce9-b93a-ca32598dd346)
10. Assign the policy to your target devices.  
11. Verify successful onboarding in the **Microsoft Defender portal**.
12. ![image](https://github.com/user-attachments/assets/0ca35576-2e90-4af9-b580-9677d6b9e6b8)


---

## 🔟 Post-Onboarding Tasks & Common Mistakes  

After onboarding, use the following resources to confirm a healthy MDE deployment:

✅ https://jeffreyappel.nl/how-to-check-for-a-healthy-defender-for-endpoint-environment  
✅ https://www.youtube.com/watch?v=_zjANEdgcpo&t=674s 
✅ https://www.youtube.com/watch?v=PBy1dxoqakY&t=343s

---

## 1️⃣1️⃣ Validating MDE Deployment  

Use these **testing tools** to verify your **Defender for Endpoint** setup:

- **[Defender Testground](https://demo.wd.microsoft.com/)** – Simulate malware detections and endpoint threats.  
- **[MDETester](https://github.com/LearningKijo/MDEtester)** – Run scripted validation tests to check **onboarding success and policy enforcement**.
- **[MDETroubleshooter](https://github.com/ThomasVrhydn/MDE-troubleshooter)** – Analyze issues related to MDE.

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
