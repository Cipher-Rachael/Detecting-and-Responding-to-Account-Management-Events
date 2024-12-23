# Detecting-and-Responding-to-Account-Management-Events

This repository contains a comprehensive guide on detecting and responding to account management events in Windows environments. Account management events, such as user account creation, deletion, or modification, provide critical insights into system activities and potential security risks. This project is designed to help administrators and SOC teams:

- Understand the importance of security logs.
- Configure security policy settings.
- Trigger specific Event IDs for testing purposes.
- Develop response strategies for account management events.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Why Security Logs Matter](#why-security-logs-matter)
3. [Configuring Security Policies](#configuring-security-policies)
4. [Viewing Security Logs](#viewing-security-logs)
5. [Event Trigger Scenarios](#event-trigger-scenarios)
6. [Best Practices](#best-practices)
7. [Contributing](#contributing)

---

## Introduction
Windows security logs are essential for monitoring system activities, detecting threats, and ensuring system integrity. This guide provides step-by-step instructions for triggering account management events and responding effectively to these alerts.

---

## Why Security Logs Matter
Security logs help:

- Detect unauthorized activities (e.g., account creation, privilege escalation).
- Audit system usage for compliance and policy adherence.
- Investigate incidents with a clear trail of evidence.
- Proactively identify and mitigate security risks.

Without detailed monitoring, organizations risk missing early warning signs of potential threats.

---

## Configuring Security Policies
To enable effective monitoring, security policies must be configured properly:

1. **Audit Policies:** Enable account management auditing.
2. **Account Lockout Policies:** Set thresholds to minimize brute-force attack risks.
3. **Group Policies:** Enforce consistent configurations across systems.
4. **Advanced Security Options:** Use multi-factor authentication and strong password policies.

### Steps to Enable Account Management Audit Policies
1. Press `Windows+R`, type `secpol.msc`, and press Enter.
2. Navigate to **Local Policies > Audit Policy**.
3. Enable auditing for account management by selecting both **Success** and **Failure**.

---

## Viewing Security Logs

### Accessing Logs in Event Viewer
1. Press `Windows+R`, type `eventvwr.msc`, and press Enter.
2. Go to **Windows Logs > Security**.
3. Analyze logs for specific Event IDs related to account management.

---

## Event Trigger Scenarios

### Common Event IDs and How to Trigger Them

- **Event ID 4720: User Account Created**
  - **Trigger:** Run `net user <username> /add`.
  - **Response:** Verify account creation, analyze logs, and disable unauthorized accounts.

- **Event ID 4722: User Account Enabled**
  - **Trigger:** Run `net user <username> /active:yes`.
  - **Response:** Confirm policy alignment and monitor account behavior.

- **Event ID 4726: User Account Deleted**
  - **Trigger:** Run `net user <username> /delete`.
  - **Response:** Investigate deletion and ensure backups are intact.

For more detailed scenarios, refer to the full guide.

---

## Best Practices

- **Continuous Monitoring:** Use SIEM tools to correlate events.
- **Automated Alerts:** Configure real-time alerts for critical Event IDs.
- **Incident Response Plan:** Develop and maintain a documented response strategy.
- **User Education:** Train employees to identify and prevent security risks.
- **Regular Audits:** Review account activities and privileges periodically.

---

## Contributing

Contributions are welcome! If you have additional scenarios, best practices, or enhancements, feel free to submit a pull request or open an issue.

---


