\# EID-EXP-001 — Create a Microsoft Entra ID Lab Tenant + Baseline Identity Setup



\## Overview

This experiment documents how to create a clean Microsoft Entra ID lab tenant and apply a baseline identity setup that is safe, repeatable, and suitable for future security experiments.



This lab is designed as the starting point for the \*\*f11.ca Entra Identity Protection series\*\* and will be referenced by all future EID experiments.



---



\## Objective

\- Create a dedicated Microsoft Entra ID lab tenant

\- Configure a secure baseline identity setup

\- Prepare the tenant for future experiments (Conditional Access, Identity Protection, MFA, risk policies, etc.)

\- Document repeatable steps + evidence



---



\## Why This Lab Matters (Real-World Value)

A large number of Entra security issues in SMB and MSP environments happen because:

\- Tenants are created without security defaults or baseline policies

\- Break-glass accounts are missing

\- Admin roles are used casually

\- MFA is not planned properly from day 1



This experiment ensures the tenant starts clean and follows good security hygiene.



---



\## Lab Environment

\- Platform: Microsoft Entra ID (Azure AD)

\- Tenant Type: Cloud-only

\- Users: Cloud identities only

\- Devices: Optional (future experiments)



---



\## Prerequisites

\- A Microsoft account (personal) OR an existing Microsoft 365 admin account

\- Ability to create a new tenant

\- A secure password manager recommended



---



\## Licensing Notes

This experiment can be completed with \*\*Microsoft Entra Free\*\*.



However, future labs in the Identity Protection series require:

\- Microsoft Entra ID P2 (or Microsoft 365 E5)



---



\## Experiment Steps



\### Step 1 — Create a New Tenant

1\. Go to Microsoft Entra admin center

2\. Create a new tenant (example naming):

&nbsp;  - Tenant name: `f11-lab-entra`

&nbsp;  - Initial domain: `f11labxxxx.onmicrosoft.com`

3\. Confirm tenant creation



\*\*Evidence to Capture\*\*

\- Tenant overview page (showing tenant name and domain)



---



\### Step 2 — Create Core Admin Accounts

Create the following accounts:



\#### 1) Primary Admin (daily admin)

\- Example: `admin@tenant.onmicrosoft.com`



\#### 2) Break-Glass Admin (Emergency only)

\- Example: `bgadmin@tenant.onmicrosoft.com`

\- Must have:

&nbsp; - Long password (30+ characters)

&nbsp; - Stored in password manager

&nbsp; - Excluded from Conditional Access policies later (carefully)



\#### 3) Test User (normal user)

\- Example: `user1@tenant.onmicrosoft.com`



\*\*Evidence to Capture\*\*

\- Users list showing the 3 accounts



---



\### Step 3 — Assign Roles (Minimal Required)

Assign roles properly:



\- Primary Admin → Global Administrator (temporary if needed)

\- Break-glass → Global Administrator

\- Test User → No admin roles



> NOTE: In real production, you should avoid permanent Global Admin.  

> For lab purposes, we will keep it simple initially.



\*\*Evidence to Capture\*\*

\- Role assignments page showing both admin accounts



---



\### Step 4 — Confirm Security Defaults Status

1\. Go to: \*\*Entra ID > Properties\*\*

2\. Locate \*\*Manage security defaults\*\*

3\. Record the status:

&nbsp;  - Enabled / Disabled



> For labs, we usually disable security defaults because we will use Conditional Access later.



\*\*Evidence to Capture\*\*

\- Security defaults setting page



---



\### Step 5 — Configure Tenant Branding (Optional)

This is optional but recommended for a clean lab.



\- Add organization name: `f11.ca Labs`

\- Add logo (optional)



\*\*Evidence to Capture\*\*

\- Branding page showing configuration



---



\### Step 6 — Baseline Admin Safety Checklist

Perform these quick validations:



\- \[ ] Break-glass account login works

\- \[ ] Break-glass password stored securely

\- \[ ] Test user can login

\- \[ ] Admin portal access confirmed



---



\## Validation / Success Criteria

This experiment is successful when:



\- A clean tenant exists for f11.ca labs

\- 2 admin accounts exist (including break-glass)

\- 1 standard user exists for testing

\- Security defaults status is documented

\- Evidence screenshots are captured



---



\## Evidence Collected

Store screenshots and logs in:





