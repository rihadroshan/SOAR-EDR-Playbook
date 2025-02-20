# SOAR-EDR Security Automated Threat Detection & Response
This **SOAR-EDR Playbook** automates threat detection, alerting, and machine isolation using **LimaCharlie, Tines, Slack, and Email**. It streamlines incident response, reducing manual effort while ensuring fast and accurate remediation. Ideal for security teams looking to enhance efficiency and minimize threats.

![diagram](/assets/diagram.png)

## Features

✅ **Automated Threat Detection** – Detects hack tools and malicious activities using **LimaCharlie**  
✅ **Real-time Alerting** – Sends alerts with detailed information via **Slack and Email**  
✅ **User Decision Workflow** – Prompts for manual confirmation before isolating a machine  
✅ **Automated Machine Isolation** – Uses **LimaCharlie** to isolate infected systems  
✅ **Incident Tracking** – Notifies teams via **Slack** if a machine is isolated or if further investigation is needed  

## Workflow Overview

1. **Detection**  
   - A machine is flagged as potentially **infected** using **LimaCharlie**.  
2. **Alerting & Notification**  
   - A detection alert is sent to **Tines**, which forwards details to **Slack and Email**.  
3. **User Decision**  
   - A prompt is sent to a user (via Slack) to decide whether to isolate the machine.  
4. **Isolation** (if confirmed)  
   - The machine is **isolated using LimaCharlie**, and the status is reported back to Slack.  
5. **Investigation Required** (if not confirmed)  
   - A message is sent to **Slack** to manually investigate the affected machine.  


| Email Alert | Slack Alert |
|------------|-------------|
| <img src="assets/email.png" alt="Email Notification" width="400"/> | <img src="assets/slack.png" alt="Slack Alert" width="400"/> |

| User Page  |
|------------|
|  <img src="assets/page.png" alt="Web UI Decision Prompt" width="400"/> |

## Technologies Used

- **LimaCharlie** – Endpoint Detection & Response (EDR)  
- **Tines** – Security Automation Platform  
- **Slack** – Team Notifications & Alerts
- **Email** – Alerting via Email
