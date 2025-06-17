# Azure-App-Service-Deployment-and-Scaling
This project focuses on deploying a web application using Azure App Service, creating deployment slots for testing, configuring autoscaling based on demand, and enabling backups for disaster recovery. We'll also set up performance monitoring and alerts.


Absolutely! Here's your updated **`README.md`** for **Project 5: Azure App Service Deployment and Scaling**, with **Step 6 modified to use HTTP Response Time** for alerting:

---

# 🌐 Project 5: Azure App Service Deployment and Scaling

**Topics Covered**: App Service, Deployment Slots, Autoscaling, Backup, Monitoring


## 💼 Scenario

A company wants to deploy a web application using Azure App Service, test in isolated slots, scale the app based on usage metrics, and ensure business continuity by configuring backups.

---

## ✅ Step-by-Step Implementation

---

### ✅ Step 1: Create an App Service

* Go to **App Services > Create**.
* Choose your **subscription**, **resource group**, and provide an **App Name**.
* Select a **Runtime Stack** (e.g., .NET, Node.js, Python).
* Choose a **pricing tier** and region.
* Review and **Create**.

📸 *App Service creation page.*

<img width="516" alt="web app creation" src="https://github.com/user-attachments/assets/2c3802c0-d7e8-462d-bd83-a7b9c2c738cf" />

---

### ✅ Step 2: Deploy the Web Application

* Use **Azure DevOps** or **GitHub Actions** to connect your repo.
* Deploy the sample app to your App Service.
* Confirm the app is running via the **App URL**.

📸 *Screenshot of deployed web app.*

---

### ✅ Step 3: Set Up Deployment Slots

* Go to **App Service > Deployment Slots > Add Slot**.
* Name the new slot `"Staging"` and create it.
* Deploy a new version of the app to the **Staging** slot.
* Use the **Swap** feature to switch staging and production after testing.

📸 *Screenshot of staging slot and swap option.*

---

### ✅ Step 4: Configure Autoscaling

* Navigate to **App Service Plan > Scale Out (App Service Plan)**.
* Enable **Autoscale**.
* Create a rule: scale out by 1 instance if **CPU > 70%** for 10 minutes.

📸 *Screenshot of autoscale rule setup.*

---

### ✅ Step 5: Backup and Restore

* Go to **App Service > Backups > Configure**.
* Choose a **storage account** and configure the **backup schedule**.
* Run a **manual backup**.
* Test restoration to verify.

📸 *Screenshot of backup configuration and success message.*

---

### ✅ Step 6: Monitor and Configure Alerts

* Navigate to **App Service > Monitoring > Alerts > New Alert Rule**.
* For the **signal name**, select **Response Time**.
* Set a **static threshold**: trigger an alert if **HTTP Response Time** is **greater than 2 seconds**.
* Set evaluation frequency to **1 minute** with a **5-minute lookback window**.
* Name the alert and set up **email notifications** or **action groups**.

📸 *Screenshot of response time alert configuration.*

---

## ✅ Completion Checklist

* [x] App Service deployed
* [x] CI/CD pipeline configured
* [x] Staging slot added and tested
* [x] Autoscaling configured
* [x] Backups enabled and verified
* [x] Monitoring and alerts (HTTP response time) set up

---

Let me know when you’re ready to build the full **Projects 1–5 portfolio** or publish this to GitHub.
