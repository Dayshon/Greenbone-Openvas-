# Greenbone-Openvas-

![image](https://github.com/user-attachments/assets/dc783e8c-b78f-4444-8850-bb99a4326a41)

In this project, I began by setting up a free Azure account, providing the necessary infrastructure to perform vulnerability management activities. I then deployed OpenVAS from the Azure Marketplace, selecting a VM with a weak configuration to simulate a vulnerable environment. After SSHing into the VM, I waited for OpenVAS to fully deploy. Once the installation was complete, I logged into the OpenVAS web interface with the default credentials and immediately changed the password for security purposes.
![image](https://github.com/user-attachments/assets/7df63765-4d6a-4b5b-b3a1-6ce41b08241c)


Next, I created a second VM, intentionally configured to be vulnerable for testing. I ensured this VM was deployed in the same region and virtual network as OpenVAS for compatibility. To make it vulnerable, I installed outdated versions of software such as Firefox, VLC, and Adobe Reader. With the vulnerable VM prepared, I configured OpenVAS to define it as a target host and created a scan task for an unauthenticated scan, which provided an overview of the system’s vulnerabilities without the need for credentials..
![image](https://github.com/user-attachments/assets/2b3f85b1-fbc8-4b57-8579-c2ca2240c5fe)
![image](https://github.com/user-attachments/assets/15449e28-f8bd-475e-b8b6-abf9fd99f10b)

I then proceeded to prepare the vulnerable VM and OpenVAS for a credentialed scan. I modified the VM settings by disabling the Windows Firewall, turning off User Account Control (UAC), enabling Remote Registry, and setting specific registry keys to facilitate in-depth scanning. In OpenVAS, I created new login credentials and cloned the original target configuration for the credentialed scan. Once the setup was complete, I executed the scan, which took longer but delivered a more comprehensive analysis of the system’s internal vulnerabilities.
![image](https://github.com/user-attachments/assets/d5846c48-05b0-4038-807d-b84e1e428525)

After receiving the scan results, I reviewed and identified critical vulnerabilities, such as outdated software and misconfigurations. I then remediated these issues by uninstalling the outdated software, applying necessary patches, and making additional security adjustments. I restarted the VM to ensure the changes were applied properly. To verify the effectiveness of the remediation, I ran the credentialed scan again and compared the results to confirm that the vulnerabilities had been resolved.
![image](https://github.com/user-attachments/assets/16303452-9baa-464d-83be-ac4f8e1b9c1d)

![image](https://github.com/user-attachments/assets/1dfe1f8e-ac6b-4980-b346-19b60bb2e9c6)

This process provided me with hands-on experience in vulnerability management, from detection to remediation. It enhanced my understanding of key cybersecurity practices such as vulnerability scanning, credentialed access, and system hardening. Throughout this project, I adhered to ethical guidelines and security best practices, ensuring a thorough and responsible approach to vulnerability management.



