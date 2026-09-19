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
| Test App | Microsoft Entra SAML Toolkit / SAML Test app (Entra gallery) |
| Test Users | Reusing KokoriLab test users from prior labs |

## 📊 Quick Summary

| Feature | What It Demonstrates | Status |
|---|---|---|
| SAML SSO Integration | Enterprise app authentication via SAML | 🔄 Not started |
| Claims Mapping | Customizing user attributes passed to the app | 🔄 Not started |
| B2B Federation | Cross-organization identity trust | 🔄 Not started |

## 🔑 Skills Demonstrated
- Enterprise application registration and SSO configuration
- SAML assertion and claims mapping
- Token/assertion troubleshooting (certificates, redirect URIs, claim errors)
- Microsoft Entra B2B collaboration and external identity federation
- Identity protocol fundamentals (SAML vs. OIDC)

## 📦 What This Lab Covers

### 1. SAML SSO Integration
*Status: not started*
- Register a test SAML application (Microsoft Entra SAML Toolkit)
- Configure SSO settings: Identifier, Reply URL, sign-on URL
- Test the full sign-in flow end-to-end

### 2. Claims Mapping
*Status: not started*
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
| *(populated as the lab progresses)* | | |

## 📋 Documentation Approach
Each stage of this lab documents:
- What I configured and why
- What errors I hit, and how I diagnosed them — not just the fix
- What I'd do differently next time

## 📅 Progress Log

### [Date] — Environment Setup
- Repo created to document the build as I go
- Next: register the Microsoft Entra SAML Toolkit test app and configure basic SSO

## 🚧 Status
🔄 In progress — environment setup phase
