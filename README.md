# 🏢 Active Directory & IAM Lab – Windows Server 2022

Ett hemmalabb där jag satte upp en komplett Active Directory-miljö från grunden för att förstå hur IAM fungerar i praktiken – hur användare skapas, hanteras och tas bort i en företagsmiljö.

---

## 🎯 Syfte

Jag ville förstå hur riktiga IT-miljöer hanterar användare, behörigheter och policys. AD är grunden i nästan alla Windows-baserade företag, och det är också direkt kopplat till moderna IAM-plattformar som Azure AD och Okta.

---

## 🛠️ Teknik & Verktyg

- Windows Server 2022 (VirtualBox)
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Windows 10 Pro (klientmaskin i samma domän)

---

## ✅ Vad jag gjorde

### 1. Grundinstallation
- Installerade Windows Server 2022 i VirtualBox
- Konfigurerade statisk IP och satte upp en ny AD-skog och domän (`lab.local`)

### 2. Organisationsstruktur
- Skapade organisationsenheter (OU) för HR, IT och Finance
- Lade till användarkonton och placerade dem i rätt OU

### 3. Grupper & RBAC
- Skapade säkerhetsgrupper per avdelning
- Tilldelade resursbehörigheter baserat på grupptillhörighet – inte individuella konton
- Testade rollbaserad åtkomstkontroll (RBAC) i praktiken

### 4. Group Policy (GPO)
- Skapade GPO för lösenordspolicy (minlängd, komplexitet, utgångstid)
- Implementerade skrivbordslåsning efter inaktivitet
- Blockerade åtkomst till kontrollpanelen för icke-admin-användare

### 5. Onboarding & Offboarding
- Simulerade onboarding: skapa konto → rätt OU → rätt grupp → verifiera åtkomst
- Simulerade offboarding: inaktivera konto → ta bort grupptillhörighet → arkivera

---

## 💡 Vad jag lärde mig

- Hur AD-struktur med OU och grupper speglar en riktig organisations behörighetsmodell
- Varför RBAC är smartare än att sätta behörigheter per individ
- Hur GPO kan styra hela miljöer centralt utan att röra varje maskin manuellt
- Kopplingen mellan on-prem AD och molnbaserade lösningar som Azure AD / Entra ID

---

## 🔗 Relaterade tekniker

`Active Directory` `IAM` `RBAC` `GPO` `Windows Server` `Onboarding` `Offboarding` `Identity Management`
# active-directory-lab
