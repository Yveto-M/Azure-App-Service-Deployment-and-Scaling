
# 🌐 Project 5: Azure App Service Deployment and Scaling

**Topics Covered**: App Service, Deployment Slots, Autoscaling, Backup, Monitoring

🧠 Summary

This project focuses on deploying a web application using Azure App Service, creating deployment slots for testing, configuring autoscaling based on demand, and enabling backups for disaster recovery. You'll also set up performance monitoring and alerts.



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

📸 *Github Actions

<img width="786" alt="github deployment" src="https://github.com/user-attachments/assets/e78535f0-37b9-4531-9bd5-2eae72dfaff5" />

<img width="512" alt="azure-git-workflows" src="https://github.com/user-attachments/assets/05de21fd-ace8-4265-aa29-6ce75b2624d7" />

📸 *deployed web app.*
<img width="779" alt="proof of app deployment" src="https://github.com/user-attachments/assets/a8431468-5a8c-4df8-a7f8-a70fb36352e5" />

---

### ✅ Step 3: Set Up Deployment Slots

* Go to **App Service > Deployment Slots > Add Slot**.
* Name the new slot `"Staging"` and create it.
* Deploy a new version of the app to the **Staging** slot.
* Use the **Swap** feature to switch staging and production after testing.

📸 *staging slot and swap option.*
<img width="789" alt="github-staging-deployment" src="https://github.com/user-attachments/assets/9b2f74d6-c9e3-46bc-812e-ac721ab3e105" />

<img width="801" alt="swap staging to pro" src="https://github.com/user-attachments/assets/a4c03bb3-1b9f-4d74-a59e-ae943dd8f413" />

---

### ✅ Step 4: Configure Autoscaling

* Navigate to **App Service Plan > Scale Out (App Service Plan)**.
* Enable **Autoscale**.
* Create a rule: scale out by 1 instance if **CPU > 70%** for 10 minutes.

📸 * autoscale rule setup.*
<img width="569" alt="scale rule" src="https://github.com/user-attachments/assets/d649eaec-b295-493f-b717-5351b854c914" />

---

### ✅ Step 5: Backup and Restore

* Go to **App Service > Backups > Configure**.
* Choose a **storage account** and configure the **backup schedule**.
* Run a **manual backup**.
* Test restoration to verify.

📸 *backup configuration and success message.*
<img width="575" alt="backup-config" src="https://github.com/user-attachments/assets/66da8d2f-d8ac-4acf-bd4b-433fe737239f" />

📸 *backup Update success message.*
<img width="737" alt="web-backup" src="https://github.com/user-attachments/assets/8decfee7-1b29-4d70-b9bd-f05044d2f1a9" />

### ✅ Step 6: Monitor and Configure Alerts

* Navigate to **App Service > Monitoring > Alerts > New Alert Rule**.
* For the **signal name**, select **Response Time**.
* Set a **static threshold**: trigger an alert if **HTTP Response Time** is **greater than 2 seconds**.
* Set evaluation frequency to **1 minute** with a **5-minute lookback window**.
* Name the alert and set up **email notifications** or **action groups**.

📸 *response time alert configuration.*
<img width="757" alt="create alert rule" src="https://github.com/user-attachments/assets/4672918b-b20f-4ad3-9e7f-8fcd99c4782f" />

<img width="714" alt="action group" src="https://github.com/user-attachments/assets/4d6f14fb-ac4c-4f4e-ad51-7373102a0024" />

<img width="744" alt="app service final alert" src="https://github.com/user-attachments/assets/c4a28310-42c7-4b5c-b14f-11131b3d0156" />

---

## ✅ Completion Checklist

* [x] App Service deployed
* [x] CI/CD pipeline configured
* [x] Staging slot added and tested
* [x] Autoscaling configured
* [x] Backups enabled and verified
* [x] Monitoring and alerts (HTTP response time) set up
