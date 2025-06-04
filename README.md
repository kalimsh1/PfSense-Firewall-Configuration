The process of setting up pfSense in VMware with a Windows device as the client involves several steps. Below is a step-by-step guide to assist in the configuration, with references to the provided images where applicable. Each step is designed to ensure a thorough and accurate setup for documentation purposes on GitHub.


1. **Download pfSense Software**: Obtain the latest stable version of pfSense from the official website. Navigate to the pfSense download page and select the appropriate version.  
   ![pfsense_download](https://github.com/user-attachments/assets/4ee9842e-17d2-4aaa-ad81-77eaa1ada2a5)


2. **Install VMware Workstation**: Ensure VMware Workstation is installed on the Windows host machine. Launch the application and create a new virtual machine.


3. **Create a New Virtual Machine**: Open the New Virtual Machine Wizard in VMware. Specify the virtual machine name and select the location for the virtual machine files.  
   ![pfsense_setup](https://github.com/user-attachments/assets/4c4599b9-d294-467b-9c9c-81b0320e2a0c)


4. **Configure Virtual Machine Hardware**: Allocate resources such as memory, processors, and network adapters. Set up two network adapters: one as NAT and one as Custom (VMnet1) for the LAN interface.  
   ![pfsense_setup2network](https://github.com/user-attachments/assets/e6ffea4f-ad89-439e-9085-e0f39e0bc500)


5. **Mount the pfSense ISO**: Attach the downloaded pfSense ISO file to the virtual machine’s CD/DVD drive. Ensure the device status is set to "Connected" and "Connect at power on" is checked.


6. **Power On the Virtual Machine**: Start the virtual machine to begin the pfSense installation process. Monitor the boot-up sequence and installation details.  
   ![Screenshot 2025-06-03 031349](https://github.com/user-attachments/assets/c40adfd4-d67e-4a51-8621-3e7f81dce445)


7. **Install pfSense**: Follow the on-screen instructions to install pfSense. Select the appropriate options, such as accepting the default settings and configuring the LAN interface.  
   ![pfsense_instaltionProcess](https://github.com/user-attachments/assets/731b2594-8bc3-4776-82b2-66c8c323eedb)


8. **Configure LAN IP Address**: During installation, set the IPv4 address for the LAN interface (192.168.1.1 with a subnet mask of 255.255.255.0 /24). Enter the subnet bit count and confirm the upstream gateway if applicable.  
      

9. **Complete Installation**: Finish the installation process and reboot the system. Click "Finished Installing" in VMware once the system boots up.  
    ![home_afterNewSetup](https://github.com/user-attachments/assets/351489eb-117f-4e79-b1ae-a18b52e8bfaa)

10. **Verify Network Connectivity**: Perform a ping test from the Windows client to the pfSense LAN IP (192.168.1.10) to ensure connectivity.
   ![Screenshot 2025-06-03 024807](https://github.com/user-attachments/assets/05c5c2f5-2349-4c13-9d31-1fce0d89fcaa)


11. **Access the pfSense WebConfigurator**: After reboot, use a web browser on the Windows client to access the pfSense WebConfigurator by entering the LAN IP address (https://192.168.1.1).  
    ![Screenshot 2025-06-03 031159](https://github.com/user-attachments/assets/e706ecaf-4184-4703-9fa7-3f9d69911b82)


13. **Check System Status**: Log in to the pfSense WebConfigurator and review the dashboard to confirm system information, interface statuses (WAN:192.168.23.132 , LAN:192.168.1.1) and uptime.  
    ![Screenshot 2025-06-03 023431](https://github.com/user-attachments/assets/8cef748b-0c1b-4338-a885-27e8d203fd7a)
    

14.Customize and Understand the pfSense Dashboard:


System Info: Shows the systems name (pfSense home.arpa), user (admin@192.168.1.10), version (2.7.2-RELEASE), and uptime. It also lists the CPU and DNS servers, helping you confirm the system is running correctly.


Interfaces: Displays WAN (192.168.23.132) and LAN (192.168.1.1) statuses, ensuring your network connections are active and properly set up.


Firewall Logs: Tracks blocked traffic (from 192.168.23.1 to 255.255.255.255 on Jun 3) helping you spot and fix security issues.


Gateways: Monitors internet connections (WAN_DHCP at 192.168.23.2, online with 0ms delay), ensuring reliable routing.


Disks: Shows storage usage (6% of 16GB used) to manage space.


Packages: Lists installed tools (arpwatch 0.2.1) for managing extra features.


Customization: Add widgets via + button to monitor specific details like traffic or logs, making it easier to focus on what matters.

![Screenshot 2025-06-03 031709](https://github.com/user-attachments/assets/18d138b8-d5dd-4175-a3b5-e835f9eeba66)
