# Kali Linux Assignment of Bootcamp

## Kali Linux References Notes

### Kali Linux Overview

- **Introduction:**  
Kali Linux is a specialized Linux distribution primarily used by ethical hackers, penetration testers, and cybersecurity professionals. It is built on Debian Linux and provides a wide array of tools and utilities for security testing and penetration testing.

- **History:**  
Previously known as Backtrack, Kali Linux was rebranded from its 6th version. It evolved into one of the most powerful and versatile platforms in cybersecurity.

- **Competitors:**
  - Parrot Security OS
  - BlackArch
  - BlackBox

### Setting Up Kali Linux on VMware

1. **Download Kali Linux OVA File:**  
   Using an OVA (Open Virtual Appliance) file is one of the easiest methods for setting up Kali Linux on VMware, as it streamlines the installation process.

2. **Steps to Set Up Kali Linux on VMware:**
   1. Download the Kali OVA file from the official Kali Linux website.
   2. Open VMware Workstation or Player.
   3. Click on **File > Open** and select the downloaded OVA file.
   4. Once the virtual machine is added, click on **Import** and wait for the process to complete.
   5. Start the Kali VM.

3. **Default Credentials:**
   - Username: **kali**
   - Password: **kali**

### Basic Kali Linux Commands

These are essential Linux commands to get started with Kali Linux:

- **ifconfig:** Display network interface details (IP address).  
  **Example:**  
	 ```bash 
		  ifconfig


-   **ping :** Check if a remote system is alive.  
    **Example:**
    
    ```bash
    ping 192.168.1.1
    
    ```
    
-   **mkdir :** Create a new folder.  
    **Example:**
    
    ```bash
    mkdir myfolder
    
    ```
    
-   **nano <FILENAME.TXT>:** Create/edit a text file (CTRL+S to save, CTRL+X to exit).  
    **Example:**
    
    ```bash
    nano myfile.txt
    
    ```
    
-   **rm -rf :** Remove a folder and its contents.  
    **Example:**
    
    ```bash
    rm -rf myfolder
    
    ```
    
-   **rm <FILENAME.TXT>:** Remove a file.  
    **Example:**
    
    ```bash
    rm myfile.txt
    
    ```
    
-   **cd :** Navigate to a folder.  
    **Example:**
    
    ```bash
    cd Documents
    
    ```
    
-   **pwd:** Show the current working directory.  
    **Example:**
    
    ```bash
    pwd
    
    ```
    
-   **whoami:** Show the current logged-in username.  
    **Example:**
    
    ```bash
    whoami
    
    ```
    
-   **reboot:** Restart the system.  
    **Example:**
    
    ```bash
    reboot
    
    ```
    
-   **cp :** Copy files.  
    **Example:**
    
    ```bash
    cp file1.txt /home/user/Documents
    
    ```
    
-   **mv :** Move files.  
    **Example:**
    
    ```bash
    mv file1.txt /home/user/Documents
    
    ```
    
-   **chmod +x _._:** Grant execution permissions to all files in a folder.  
    **Example:**
    
    ```bash
    chmod +x *.sh
    
    ```
    
-   **bash <FILENAME.sh>:** Run a shell script.  
    **Example:**
    
    ```bash
    bash script.sh
    
    ```
    
-   **python <FILENAME.py>:** Run a Python script.  
    **Example:**
    
    ```bash
    python myscript.py
    
    ```
    
-   **macchanger -s eth0:** Show the current MAC address.  
    **Example:**
    
    ```bash
    macchanger -s eth0
    
    ```
    
-   **ls:** List contents of a directory.  
    **Example:**
    
    ```bash
    ls
    
    ```
    
-   **git clone <GITHUB_LINK>:** Clone a repository from GitHub.  
    **Example:**
    
    ```bash
    git clone https://github.com/username/repository.git
    
    ```
    
-   **history:** Display a list of previously entered commands.  
    **Example:**
    
    ```bash
    history
    
    ```
    
-   **clear:** Clear the terminal screen.  
    **Example:**
    
    ```bash
    clear
    
    ```
    
-   **exit:** Exit the terminal.  
    **Example:**
    
    ```bash
    exit
    
    ```
    

### Root User and General User Management

-   **$:** General User
-   **#:** Root (Admin) User

1.  **Change Root User Password:**
    
    -   Command: `sudo passwd root`
    -   Enter a new root password.
2.  **User Management in Kali Linux:**
    
    -   Create a user: `useradd <USERNAME>` **Example:**
        
        ```bash
        useradd john
        
        ```
        
    -   Delete a user: `userdel <USERNAME>` **Example:**
        
        ```bash
        userdel john
        
        ```
        
    -   Change a user’s password: `passwd <USERNAME>` **Example:**
        
        ```bash
        passwd john
        
        ```
        

### File Sharing with Windows on VMware

1.  **Enable Shared Folders in VMware:**
    
    -   Go to **VM > Settings > Options**.
    -   Under the **Shared Folders** section, select **Always enabled** or **Map as a network drive in Windows guests**.
    -   Add a folder to share between Kali Linux and the Windows host.
2.  **Verify Shared Folders:**
    
    -   Shared folders will appear in the File System in Kali Linux.

### Network Settings

1.  **NAT or Bridged Adapter:**
    -   **Bridged:** Connects Kali Linux to the same network as your host.
    -   **NAT:** Shares the host's network connection.

### File Permissions in Kali Linux

1.  **Changing File Permissions:**  
    Use chmod to change file permissions. Example: `chmod +x *.*` – This grants execution permissions to all files in a folder.

### Installing Software

#### From GitHub:

1.  **Clone a GitHub Repository:**
    
    -   Search for the desired tool (e.g., EasySploit) on GitHub.
    -   Copy the GitHub repository URL.
    -   In terminal, type:
        
        ```bash
        git clone <GITHUB_LINK>
        
        ```
        
2.  **Make Files Executable:**
    
    -   Navigate to the folder: `cd <TOOLNAME>`
    -   Run: `chmod +x *.*` to make the files executable.
3.  **Run the Tool:**
    
    -   For `.sh` files: `bash <FILENAME.sh>`
    -   For `.py` files: `python <FILENAME.py>`
4.  **Install Dependencies (if required):** If a requirements.txt file exists, install dependencies using:
    
    ```bash
    pip install -r requirements.txt
    
    ```
    

#### From Kali Repositories:

1.  **Use the apt package manager to install tools from the official Kali repositories.**
    
    Example:
    
    ```bash
    apt install tor
    apt install wireshark
    apt install openssh-server
    
    ```
    

### Tools to Install:

-   **EasySploit:** A toolkit for exploiting web vulnerabilities.
-   **EasyMacChanger:** A tool to change the MAC address.
-   **OSI (Open Source Intelligence):** Tool for collecting OSINT data.
-   **Sherlock:** A tool to find usernames across social media platforms.
-   **Slowloris:** A denial of service tool.
-   **Hulk:** A denial of service tool.
-   **XLR8:** A tool for cracking passwords.
-   **Zphisher:** A phishing tool for social engineering attacks.
-   **Cupp:** A common user password profiler.
-   **Camphish:** A phishing tool for camouflaging.


***This document has been created as part of the Kali Linux bootcamp assignment. It provides a comprehensive overview of key concepts and tools learned throughout the course. The MD file was crafted using StackEdit, a versatile Markdown editor, available at [Stackedit.io](https://stackedit.io/app#), to offer a well-organized and accessible reference for capturing and organizing the important aspects of Kali Linux for easy future use.
It is easy and saves a lot of time***
