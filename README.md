# **Linux For Docker Project**

## **Table of Contents**

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Installation Guide](#installation-guide)
   - [Step 1: Install Windows Subsystem for Linux (WSL)](#step-1-install-windows-subsystem-for-linux-wsl)
   - [Step 2: Install a Linux Distribution](#step-2-install-a-linux-distribution)
   - [Step 3: Install Docker](#step-3-install-docker)
   - [Step 4: Configure Docker to Use WSL](#step-4-configure-docker-to-use-wsl)
4. [Running Docker on WSL](#running-docker-on-wsl)
5. [Troubleshooting](#troubleshooting)
6. [Additional Resources](#additional-resources)
7. [License](#license)

---

## **Introduction**

This project documents the process of using the latest version of WSL (Windows Subsystem for Linux) to run Docker Engine, providing a seamless development environment for containerized applications. The goal is to help developers set up Docker on WSL for efficient and streamlined development on Windows.

---

## **Prerequisites**

Before you begin, ensure that you have the following:

- A machine running Windows 10 or later.
- Administrative privileges to install and configure WSL and Docker.
- An active internet connection to download required software and updates.

---

## **Installation Guide**

### **Step 1: Install Windows Subsystem for Linux (WSL)**

1. **Enable WSL:**
   - Open PowerShell as Administrator.
   - Run the following command to enable WSL:
     ```powershell
     wsl --install
     ```
   - Restart your computer if prompted.

2. **Check WSL Version:**
   - Ensure that WSL 2 is installed by running:
     ```powershell
     wsl --list --verbose
     ```
   - The output should indicate that WSL 2 is set as the default version.

![WSL Installation Screenshot](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

### **Step 2: Install a Linux Distribution**

1. **Choose a Linux Distribution:**
   - Open the Microsoft Store and search for your preferred Linux distribution (e.g., Ubuntu).
   - Click "Install" to download and install the distribution.

2. **Set Up the Distribution:**
   - After installation, launch the Linux distribution.
   - Follow the on-screen instructions to set up a username and password.

![Linux Distribution Setup Screenshot](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

### **Step 3: Install Docker**

1. **Update Your Package List:**
   - Open your Linux terminal in WSL.
   - Run the following commands:
     ```bash
     sudo apt-get update
     sudo apt-get upgrade
     ```

2. **Install Docker:**
   - Install Docker by running:
     ```bash
     sudo apt-get install docker.io
     ```
   - Start Docker with:
     ```bash
     sudo service docker start
     ```

![Docker Installation Screenshot](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

### **Step 4: Configure Docker to Use WSL**

1. **Add Your User to the Docker Group:**
   - Run the following command to avoid using `sudo` with Docker:
     ```bash
     sudo usermod -aG docker $USER
     ```
   - Log out and back in for the changes to take effect.

2. **Verify Docker Installation:**
   - Check that Docker is installed correctly by running:
     ```bash
     docker --version
     ```

![Docker Version Screenshot](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

---

## **Running Docker on WSL**

Now that Docker is installed and configured on WSL, you can run Docker commands just as you would on a native Linux system.

- **Running a Test Container:**
  ```bash
  docker run hello-world
  ```
  This command downloads a test image and runs it in a container, verifying that Docker is working correctly.

![Hello World Docker Screenshot](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

---

## **Troubleshooting**

### **Common Issues and Fixes:**

- **Docker Daemon Not Starting:**
  - Ensure that the Docker service is running:
    ```bash
    sudo service docker start
    ```

- **Permission Denied Errors:**
  - Ensure your user is added to the Docker group and you have logged out and back in after making changes.

![Troubleshooting Screenshot](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

---

## **Additional Resources**

- **Tutorial Video:** [David Bombal on Installing WSL](https://youtu.be/_fntjriRe48?si=EjwkaAGNsuMSPJOj)
- **Docker Documentation:** [Docker Official Documentation](https://docs.docker.com/)
- **WSL Documentation:** [Microsoft WSL Documentation](https://docs.microsoft.com/en-us/windows/wsl/)

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

![MIT License](https://user-images.githubusercontent.com/your-username/path-to-your-image.png)

---
