# 🔗 SSO & Federation Lab
### SAML · OIDC · Enterprise App Integration · B2B Federation

> One-line takeaway: Building a hands-on lab covering single sign-on and federation — configuring enterprise application authentication, claims mapping, and cross-organization identity trust in a Microsoft 365 tenant.

![Entra ID](https://img.shields.io/badge/Entra%20ID-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![SAML](https://img.shields.io/badge/SAML-FF6600?style=for-the-badge&logo=data:image/png;base64,&logoColor=white)
![OIDC](https://img.shields.io/badge/OIDC-000000?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=for-the-badge)

## 🎯 Goal
Building a hands-on lab demonstrating single sign-on (SSO) and identity federation —
integrating an enterprise application via SAML, understanding claims mapping and token
flow, and configuring cross-organization trust — in a Microsoft 365 tenant.

## 🧱 Environment
| Component | Details |
|---|---|
| Tenant | Microsoft 365 with Entra ID P2 (Trial) |
| Test App | Microsoft Entra SAML Toolkit ("KokoriLab SAML Test App") — samltoolkit.azurewebsites.net |
| Test Users | Sarah Chen assigned for SSO testing; reusing KokoriLab test users from prior labs |

## 📊 Quick Summary

| Feature | What It Demonstrates | Status |
|---|---|---|
| SAML SSO Integration | Enterprise app authentication via SAML | ✅ Complete |
| Claims Mapping | Customizing user attributes passed to the app | ✅ Complete |
| B2B Federation | Cross-organization identity trust | 🔄 Not started |

## 🔑 Skills Demonstrated
- Enterprise application registration and SSO configuration
- SAML assertion and claims mapping
- Token/assertion troubleshooting (certificates, redirect URIs, claim errors)
- Microsoft Entra B2B collaboration and external identity federation
- Identity protocol fundamentals (SAML vs. OIDC)

## 📦 What This Lab Covers

### 1. SAML SSO Integration
*Status: ✅ Complete*
- Register a test SAML application (Microsoft Entra SAML Toolkit)
- Configure SSO settings: Identifier, Reply URL, sign-on URL
- Test the full sign-in flow end-to-end

### 2. Claims Mapping
*Status: ✅ Complete*
- Customize which user attributes are sent to the application
- Add/modify claim rules
- Verify claims in the SAML response

### 3. B2B Federation
*Status: not started*
- Configure external collaboration settings
- Invite a guest user from another identity provider (e.g. Google)
- Document the federated sign-in experience

## 🛠️ Notable Troubleshooting
| Issue | Root Cause | Resolution |
|---|---|---|
| Redirected to SAML Toolkit but sign-in wasn't recognized | SSO doesn't automatically create app-side accounts — the toolkit requires a matching user to already exist on its own site | Registered a matching account on the SAML Toolkit using the same email as the Entra ID identity |

## 📋 Documentation Approach
Each stage of this lab documents:
- What I configured and why
- What errors I hit, and how I diagnosed them — not just the fix
- What I'd do differently next time

## 📅 Progress Log
### September 20, 2026 — SAML SSO Integration Completed
- Registered the Microsoft Entra SAML Toolkit from the Entra ID app gallery as
  "KokoriLab SAML Test App" — a Microsoft-provided test app for practicing real
  SAML integration patterns
- Configured Basic SAML Configuration: Identifier (Entity ID), Reply URL (ACS), and
  Sign on URL, matching the toolkit's documented values
- Reviewed default Attributes & Claims (givenname, surname, emailaddress, name,
  Unique User Identifier), then added a custom "Department" claim mapped to
  user.department to demonstrate claims mapping beyond the defaults
- Assigned Sarah Chen as a test user for the application
- Confirmed the SAML signing certificate was Active
- Discovered SSO requires a matching user account to exist on the target application
  itself — registered a matching account on the SAML Toolkit site using the same
  email as the Entra ID identity
- Completed the toolkit's own SAML configuration by copying Entra ID's Login URL,
  Microsoft Entra Identifier, Logout URL, and the downloaded raw certificate into
  the toolkit's setup form — establishing the trust relationship
- Successfully completed a full, live SP-initiated SSO sign-in: toolkit login page →
  redirected to Microsoft for authentication → signed in with KokoriLab credentials →
  redirected back to the toolkit, fully authenticated
- Full SAML SSO round trip demonstrated end-to-end

### September 19, 2026 — Environment Setup
- Repo created to document the build as I go
- Next: register the Microsoft Entra SAML Toolkit test app and configure basic SSO

## 🚧 Status

🔄 **In Progress** — 2 of 3 components complete

| Component | Status |
|---|---|
| SAML SSO Integration | ✅ Complete |
| Claims Mapping | ✅ Complete |
| B2B Federation | 🔄 Remaining |
