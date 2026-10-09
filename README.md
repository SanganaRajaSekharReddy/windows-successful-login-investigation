# Windows Successful Login Investigation

## Project Overview

This is a beginner SOC Analyst project using Windows Event Viewer to investigate successful Windows login events.

## Objective

The objective is to understand Windows authentication logs and learn how SOC Analysts review successful login activity.

## Tool Used

* Windows Event Viewer
* Windows Security Logs

## Event Investigated

**Event ID 4624 — Successful Logon**

## Findings

| Field                  | Finding                          |
| ---------------------- | -------------------------------- |
| Event ID               | 4624                             |
| Account                | SYSTEM                           |
| Computer               | chandu                           |
| Logon Type             | 5 — Service Logon                |
| Process                | C:\Windows\System32\services.exe |
| Authentication Package | Negotiate                        |
| Result                 | Successful logon                 |

## Investigation

I filtered Windows Security Logs using Event ID 4624 and reviewed the event details.

The event showed a successful service logon by the built-in SYSTEM account. Logon Type 5 is associated with service logons.

This activity appears consistent with normal Windows service activity. The event alone does not confirm suspicious behavior.

## Screenshots

### Successful Login — General Information

![Event ID 4624](screenshots/01-successful-login-general.png)

### Successful Login — Detailed Information

![Event Details](screenshots/02-successful-login-details.png)

## What I Learned

* How to filter Windows Security Logs.
* What Event ID 4624 means.
* How to identify Logon Type 5.
* How to review process and authentication details.
* How to document findings from a basic SOC investigation.

## Conclusion

This task gave me hands-on practice investigating Windows authentication logs using Event Viewer as part of my SOC Analyst learning journey.

**Environment:** My own Windows computer
**Project Type:** Beginner SOC Analyst Lab
