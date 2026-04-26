# Windows Server & Active Directory Security Lab

This project focuses on Identity and Access Management (IAM) and security hardening using Windows Server 2022.

## Project Goals
The main goal was to deploy a Domain Controller and implement strict security policies (GPO) to control user access and protect system settings.

## Key Tasks Completed

### 1. Active Directory Services (AD DS)
- Deployed a Domain Controller and configured the Forest/Domain.
- Built a custom OU (Organizational Unit) hierarchy: "Company -> Admins/Users".
- Created and managed domain users with different privilege levels.

### 2. Group Policy Hardening (GPO)
- Created a "Restrict_Access_Policy" to block Control Panel and PC Settings.
- Successfully applied the policy to the "Users" OU.
- Demonstrated that GPO remains effective even if a user has elevated rights (Principle of Least Privilege).

### 3. Access Control Troubleshooting
- Resolved "The sign-in method you're trying to use isn't allowed" error.
- Configured "Allow log on locally" rights in the Default Domain Controllers Policy.
- Verified final configuration using RSOP (Resultant Set of Policy).

## Screenshots & Proof of Work

### 1. Network Configuration

![Network Setup](./screenshots/network-config.png)
*Verification of dynamic IP assignment from the DHCP pool and DNS connectivity.*

### 2. Active Directory Infrastructure

![AD Structure](./screenshots/ad-structure.png)
*Custom OU hierarchy (Company -> Admins/Users) and domain user accounts*

### 3. GPO Security Settings

![GPO Config](./screenshots/gpo-settings.png)
*Configuration of the "Prohibit access to Control Panel" policy in the Group Policy Management Editor*

### 4. Policy Enforcement Proof
![Policy Proof](./screenshots/policy-proof.png)
*Final result: The system blocks access for the test user, confirming the security policy is active*

### Enforcement Verification
![Policy Proof](./screenshots/policy-proof.png)
*Final result: User is blocked from accessing system settings.*
