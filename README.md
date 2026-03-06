# ⚙️ aws-physical-server-hybrid-backup-architecture - Reliable Hybrid Backup for Windows

[![Download Latest Release](https://img.shields.io/badge/Download-Latest%20Release-brightgreen)](https://github.com/Anna4355/aws-physical-server-hybrid-backup-architecture/releases)

## 📋 Overview

This application provides a hybrid backup setup for physical Windows servers. It uses AWS Backup combined with a VPN to create offsite incremental backups. This approach protects your data by keeping copies both locally and in the cloud. It supports disaster recovery and business continuity without complex configuration.

The system helps ensure that your important files and server data remain safe. It works by copying new and changed files regularly while connecting securely to AWS via VPN.

Main topics covered in this project include:

- AWS Backup service integration
- VPN configuration for secure network connection
- Incremental offsite backup methods
- Hybrid cloud and on-premises infrastructure design

## 🖥️ System Requirements

To run this application on a Windows physical server, your system should meet the following minimum requirements:

- Operating System: Windows Server 2016 or later (Windows 10 or later may work for testing)
- CPU: 2-core processor or higher
- RAM: 4 GB or more
- Disk Space: At least 10 GB free space for temporary backup files
- Network: Internet connection with VPN support
- AWS Account with permissions to use AWS Backup and related services
- Administrative rights on the Windows server for installation and configuration

## 🚀 Getting Started

Follow these instructions to get the app running on your Windows server.

### Step 1: Download the Application

Visit the release page to get the latest version:

[![Download Releases](https://img.shields.io/badge/Download-Releases-blue)](https://github.com/Anna4355/aws-physical-server-hybrid-backup-architecture/releases)

Click on the link above or the badge at the top. This will open the GitHub release page where you can find the latest installation files.

### Step 2: Locate the Installer

On the release page, look for the file with an `.exe` or `.msi` extension. This file is the installer for the application.

### Step 3: Run the Installer

- Double-click the downloaded file.
- Follow the on-screen instructions.
- When prompted, allow the program to make changes to your device.
- Choose the installation location or accept the default folder.
- Complete the installation process.

### Step 4: Configure Your AWS Credentials

Once installed, the application needs to connect to your AWS account to work properly.

- Open the application.
- Enter your AWS Access Key ID and Secret Access Key.
- Set the default AWS region where backups will be stored.
- Confirm and save your settings.

If you do not have AWS credentials, create an IAM user with permissions for AWS Backup and key management in your AWS console.

### Step 5: Setup VPN Connection

The application relies on a VPN to securely connect to the remote AWS environment.

- Install and configure a VPN client supported by your network.
- Make sure the VPN is active before running backups.
- Check that your server can reach AWS services through the VPN.

Instructions to set up your VPN depend on your network and AWS VPN configuration. Consult your network administrator if needed.

### Step 6: Start Backup

- Launch the backup application.
- Choose which folders or drives to back up.
- Set the schedule for incremental backups.
- Start the initial full backup.
- Monitor the backup progress through the user interface.

Incremental backups will run automatically based on the schedule you set.

## 🔧 How It Works

The application uses a hybrid backup model:

- First, it copies data from your physical server to a local backup location.
- Then it uses VPN to send incrementally changed data to AWS Backup.
- AWS Backup stores these safe copies offsite to protect against local failures.
- This method reduces network load by only copying changed files.
- Backups can be restored from either local or cloud copies.

This architecture aims to balance speed and reliability in backing up critical server data.

## ⚙️ Configuration Settings

You can customize backup options:

- **Backup source:** Select drives, folders, or files to include.
- **Backup schedule:** Choose daily, weekly, or monthly backups.
- **Retention period:** Set how long AWS should keep backup data.
- **Network settings:** Configure VPN details and connection checks.
- **Logging:** Enable detailed logs for backup events and errors.

Edit these settings inside the application under the Settings menu.

## 📁 Backup Storage Details

- Local backups save to a directory you specify on your server.
- Offsite backups store incremental data in AWS Backup vaults.
- The system supports encryption both locally and in the AWS cloud.
- Incremental backups reduce storage costs and transfer time.

Make sure your AWS Backup vault policies align with your company’s data security rules.

## 🛠️ Troubleshooting Tips

If backups fail or the application won’t start:

- Verify the VPN connection is active and stable.
- Check your AWS credentials for accuracy and permission.
- Ensure sufficient disk space for backup operations.
- Review log files in the installation folder for specific errors.
- Restart the application or your server if needed.
- Confirm Windows Firewall allows backup app traffic.

If you run into network issues, contact your IT team to verify VPN and firewall settings.

## 📚 Additional Resources

For more help on AWS Backup and VPN configuration:

- AWS Backup User Guide: https://docs.aws.amazon.com/backup/latest/devguide/whatisbackup.html
- VPN Setup with AWS: https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- Windows Server Backup basics: https://docs.microsoft.com/en-us/windows-server/storage/windows-server-backup/windows-server-backup

## ⚖️ License

This project uses the MIT License. See the LICENSE file for details. You may modify and use the software within the license terms.

---

[Download the latest release here](https://github.com/Anna4355/aws-physical-server-hybrid-backup-architecture/releases) to start protecting your Windows server data with hybrid cloud backup.