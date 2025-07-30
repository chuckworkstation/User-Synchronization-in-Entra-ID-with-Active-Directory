# User-Synchronization-in-Entra-ID-with-Active-Directoy 

This guide outlines the key steps to **install Active Directory Domain Services (AD DS)** and **promote a Windows Server to a Domain Controller**, laying the foundation for synchronizing with **Microsoft Entra ID (formerly Azure AD)**.Therefore connecting On-prem to the Cloud.

---

## 📝 Prerequisites

Before you begin, ensure you have:

- ✅ A valid Microsoft Entra ID (Azure AD) tenant  
- ✅ A Windows Server 2016 or later (local or VM)  
- ✅ Internet access on the server  
- ✅ Admin credentials for both the Entra ID tenant and Windows Server  

---

## 🪜 Step-by-Step Instructions

### 1. Open Server Manager
- Click the **Start Menu**  
- Select **Server Manager**

### 2. Add Roles and Features
- In Server Manager, click **Add roles and features**  
- Select **Role-based or feature-based installation**  
- Click **Next** to confirm the server selection  

### 3. Install Active Directory Domain Services (AD DS)
- In the **Server Roles** section, check **Active Directory Domain Services**  
- When prompted, click **Add Features**  
- Click **Next** through remaining steps  
- Click **Install**

### 4. Promote Server to a Domain Controller
- After installation, click the ⚠️ icon in Server Manager  
- Select **Promote this server to a domain controller**  
- Choose **Add a new forest** and enter your domain name (e.g., `labdomain.local`)  
- Set a **DSRM (Directory Services Restore Mode) password**  
- Click **Next** through the configuration steps  
- Click **Install**

> 🔄 The server will automatically reboot after promotion.

---

## ✅ What You’ve Accomplished

You’ve now successfully:

- Installed AD DS on your Windows Server  
- Created a new Active Directory forest  
- Promoted your server to a Domain Controller  

This environment is now ready to be connected to your Entra ID tenant for **Cloud Sync testing**, which will be covered in the next phase of the lab.

