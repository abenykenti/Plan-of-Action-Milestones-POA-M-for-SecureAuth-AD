# Plan of Action & Milestones (POA&M) for SecureAuth-AD

## Overview
This Plan of Action and Milestones (POA&M) addresses the findings from the SecureAuth-AD audit, conducted against the NIST 800-53 and ISO 27001 standards. The audit identified gaps in the implementation of account lockout policies, which are essential for preventing unauthorized access through brute force attacks.

---

## 1. Finding: Non-implementation of Account Lockout Policy (NIST 800-53 AC-7)

- **Control ID:** AC-7
- **Control Family:** Access Control
- **Audit Standard:** NIST 800-53
- **Control Requirement:** Implement account lockout after a specified number of unsuccessful login attempts within a set time.
- **Finding:** No account lockout policy was implemented in SecureAuth-AD, creating a vulnerability to brute force attacks.

### Corrective Actions:
- **Action Plan:** Implement a Group Policy Object (GPO) to enforce account lockout after 5 unsuccessful attempts within 15 minutes.
- **Resource Assignment:** SecureAuth-AD administrator team
- **Completion Date:** 2024-10-20
- **Milestones:**
  1. **2024-10-10** - Define account lockout thresholds and duration.
  2. **2024-10-15** - Implement GPO and configure monitoring.
  3. **2024-10-20** - Test and validate the configuration.

---

## 2. Finding: Lack of Secure Logon Procedures (ISO 27001 A.9.4.2)

- **Control ID:** A.9.4.2
- **Control Family:** Secure Logon Procedures
- **Audit Standard:** ISO 27001
- **Control Requirement:** Ensure failed login attempts trigger account lockout to prevent unauthorized access.
- **Finding:** SecureAuth-AD did not enforce secure logon procedures, specifically account lockout, after multiple failed login attempts.

### Corrective Actions:
- **Action Plan:** Set up a GPO to lock accounts after 5 failed login attempts, with an automatic reset after 30 minutes.
- **Resource Assignment:** SecureAuth-AD administrator team
- **Completion Date:** 2024-10-20
- **Milestones:**
  1. **2024-10-12** - Configure account lockout settings for user authentication.
  2. **2024-10-16** - Test the lockout process to ensure compliance.
  3. **2024-10-20** - Document results and ensure long-term monitoring.

---

## Monitoring and Continuous Compliance

- **Responsible Team:** IT Security & Compliance
- **Review Frequency:** Monthly (beginning 2024-11-01)
- **Follow-Up Actions:** 
  - Continuous monitoring via event logs to ensure account lockout controls remain operational.
  - Quarterly audits to ensure ongoing compliance with both NIST 800-53 AC-7 and ISO 27001 A.9.4.2.

---

## Conclusion:
The SecureAuth-AD system currently has vulnerabilities related to account lockout policies. By implementing the recommended corrective actions and adhering to the outlined milestones, SecureAuth-AD will achieve compliance with NIST 800-53 and ISO 27001 standards, reducing risks associated with unauthorized access.

📄 **[Download Full POA&M (PDF)](link_to_poam_pdf)**

