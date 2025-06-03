The process of setting up pfSense in VMware with a Windows device as the client involves several steps. Below is a step-by-step guide to assist in the configuration, with references to the provided images where applicable. Each step is designed to ensure a thorough and accurate setup for documentation purposes on GitHub.

1. **Download pfSense Software**: Obtain the latest stable version of pfSense from the official website. Navigate to the pfSense download page and select the appropriate version (e.g., 2.7.2-RELEASE).  
   ![pfsense_download](https://github.com/user-attachments/assets/4ee9842e-17d2-4aaa-ad81-77eaa1ada2a5)


2. **Install VMware Workstation**: Ensure VMware Workstation Pro (e.g., version 17) is installed on the Windows host machine. Launch the application and create a new virtual machine.

3. **Create a New Virtual Machine**: Open the New Virtual Machine Wizard in VMware. Specify the virtual machine name (e.g., "pfSense-FW2") and select the location for the virtual machine files (e.g., C:\Users\AdminOneDrive\Documents\Virtual Machines\pfSense-FW2).  
   - Photo Reference: [Photo 7]

4. **Configure Virtual Machine Hardware**: Allocate resources such as memory (e.g., 3.7 GB), processors, and network adapters. Set up two network adapters: one as NAT and one as Custom (VMnet1) for the LAN interface.  
   - Photo Reference: [Photo 16]

5. **Mount the pfSense ISO**: Attach the downloaded pfSense ISO file to the virtual machine’s CD/DVD (IDE) drive. Ensure the device status is set to "Connected" and "Connect at power on" is checked.

6. **Power On the Virtual Machine**: Start the virtual machine to begin the pfSense installation process. Monitor the boot-up sequence and installation details.  
   - Photo Reference: [Photo 15]

7. **Install pfSense**: Follow the on-screen instructions to install pfSense. Select the appropriate options, such as accepting the default settings and configuring the LAN interface.  
   - Photo Reference: [Photo 14]

8. **Configure LAN IP Address**: During installation, set the IPv4 address for the LAN interface (e.g., 192.168.1.1 with a subnet mask of 255.255.255.0 /24). Enter the subnet bit count (e.g., 24) and confirm the upstream gateway if applicable.  
   - Photo Reference: [Photo 2]

9. **Enable DHCP Server (Optional)**: Choose whether to enable the DHCP server on the LAN interface. If enabled, specify the start address of the IPv4 client address range.  
   - Photo Reference: [Photo 2]

10. **Complete Installation**: Finish the installation process and reboot the system. Click "Finished Installing" in VMware once the system boots up.  
    - Photo Reference: [Photo 13]

11. **Access the pfSense WebConfigurator**: After reboot, use a web browser on the Windows client to access the pfSense WebConfigurator by entering the LAN IP address (e.g., https://192.168.1.1).  
    - Photo Reference: [Photo 17]

12. **Verify Network Connectivity**: Perform a ping test from the Windows client to the pfSense LAN IP (e.g., 192.168.1.10) to ensure connectivity.  
    - Photo Reference: [Photo 1]

13. **Configure Interfaces**: Assign and configure the WAN and LAN interfaces in the pfSense console or WebConfigurator. Verify the interface settings match the intended network configuration.  
    - Photo Reference: [Photo 12]

14. **Check System Status**: Log in to the pfSense WebConfigurator and review the dashboard to confirm system information, interface statuses (e.g., WAN: 192.168.23.132, LAN: 192.168.1.1), and uptime.  
    - Photo Reference: [Photo 17]

This guide provides a comprehensive sequence for setting up pfSense in a VMware environment, with specific steps aligned to the provided images for clarity and documentation.
