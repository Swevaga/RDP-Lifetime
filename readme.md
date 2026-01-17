# RDP-Lifetime (VPSBYEVAGA)

<div align="center">

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Evaga/RDP-Lifetime/main.yml?branch=main&style=for-the-badge)
![Tailscale](https://img.shields.io/badge/Network-Tailscale-blue?style=for-the-badge&logo=tailscale)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**Automated Windows RDP Environment via GitHub Actions & Tailscale Networking.**

</div>

---

## 📖 What is RDP?

**Remote Desktop Protocol (RDP)** is a proprietary protocol developed by Microsoft which provides a user with a graphical interface to connect to another computer over a network connection. 

**RDP-Lifetime** is an automation project that leverages GitHub Actions infrastructure to provision a Windows RDP instance for various testing and development purposes.

> [!WARNING]
> **Session Timeout:** GitHub Actions has a maximum execution limit. Each session will run for approximately **3 hours** before being automatically reset by the system.

---

## 🚀 Quick Start Guide

Follow these steps carefully to deploy your instance:

### 1. Account Preparation
* Create a [GitHub](https://github.com/) account.
* Sign up for [Tailscale](https://tailscale.com/) (Login via GitHub is recommended).

### 2. Generate Tailscale Auth Key
* Navigate to **Tailscale Admin Console** > **Settings** > **Keys**.
* Click **Generate Auth Key**.
* Copy and save the key (usually starts with `tskey-auth-...`).

### 3. Repository Configuration
* Create a new repository named: `VPSBYEVAGA`.
* Go to the **Settings** tab of your repository.
* Select **Secrets and Variables** > **Actions** > **New Repository Secret**.
* Configure the secret as follows:
    * **Name:** `TAILSCALE_AUTH_KEY`
    * **Secret:** (Paste your Tailscale Auth Key here).

### 4. Deploy Workflow
* Click the **Actions** tab.
* Select **"Setup a workflow yourself"**.
* Copy the YAML code from the `RDP V1.1` file in this repository and paste it into the editor.
* Click **Commit Changes**.

### 5. Running the Instance
* Navigate back to the **Actions** tab.
* Select the **RDP By Evaga** workflow on the left sidebar.
* Click **Run Workflow** > Confirm by clicking the green **Run Workflow** button.
* Wait for the process to initialize.
* Follow the **Authenticate Tailscale** link in the logs if prompted.

---

## 💻 Connection Details

Once the workflow is active, connect using the **Remote Desktop Connection** client:

1.  **Computer/IP:** Find the IP address in your Tailscale Dashboard.
2.  **Username:** (As provided in the GitHub Actions logs).
3.  **Password:** (As provided in the GitHub Actions logs).

---

## 🛠 Built With

* **GitHub Actions** - Infrastructure as Code (IaC) provider.
* **Tailscale** - Secure Mesh VPN for zero-config networking.
* **Windows Server VM** - The core remote operating system.

---

## ⚠️ Disclaimer

This project is for educational purposes only. The author is not responsible for any misuse of GitHub Actions resources. Please ensure your usage complies with the [GitHub Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service) to avoid account suspension.

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for the full license text.

---

<div align="center">
  Developed with ❤️ by <a href="https://github.com/Evaga">Evaga</a>
</div>
