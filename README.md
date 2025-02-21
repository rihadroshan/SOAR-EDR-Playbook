# SOAR-EDR Security Automated Threat Detection & Response
This **SOAR-EDR Playbook** automates threat detection, alerting, and machine isolation using **LimaCharlie, Tines, Slack, and Email**. It streamlines incident response, reducing manual effort while ensuring fast and accurate remediation. Ideal for security teams looking to enhance efficiency and minimize threats.

![diagram](/assets/diagram.png)

## Features

**Automated Threat Detection** – Detects hack tools and malicious activities using **LimaCharlie**  
**Real-time Alerting** – Sends alerts with detailed information via **Slack and Email**  
**User Decision Workflow** – Prompts for manual confirmation before isolating a machine  
**Automated Machine Isolation** – Uses **LimaCharlie** to isolate infected systems  
**Incident Tracking** – Notifies teams via **Slack** if a machine is isolated or if further investigation is needed  

## **Workflow Overview**
1. **Threat Detection**
   - The system detects a compromised endpoint using **LimaCharlie**.
   - A threat detection alert is generated and sent to **Tines**.

2. **Alerting & Notification**
   - Tines processes the detection alert and sends real-time notifications via **Slack** and **Email**.

3. **User Decision Prompt**
   - The user is prompted via a web UI (powered by Tines) to decide whether to isolate the compromised machine.
   - The user chooses between:
     - **Yes** → The machine is isolated using **LimaCharlie**.
     - **No** → An investigation alert is sent to **Slack** for further review.

4. **Automated Machine Isolation (If Confirmed)**
   - If the user confirms isolation, LimaCharlie isolates the machine.
   - A confirmation message is sent via **Slack**.

5. **Manual Investigation Required (If Not Confirmed)**
   - If the user declines isolation, a notification is sent to **Slack** indicating further investigation is required.

## **Alert Examples**
### **Email Alert**
An email notification is sent to security teams, providing details about the detected threat, including:
- Detection Type
- Timestamp
- Affected Host
- Source IP
- User Account
- File Location
- Command Executed
- Sensor ID

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
