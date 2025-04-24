# Network-Router-Security-Configuration-Lab-

### OBJECTIVE
The purpose of this lab was to get comfortable setting up network equipment like routers from scratch.I set up and protected access to the routers using basic password features in Cisco Packet Tracer. 
I connected two routers (R1 and R2) via their GigabitEthernet interfaces and created hostnames for the routers as well.Then, I set and and protected access to the routers using basic password features in Cisco Packet Tracer.Next,I turned password encryption on and off to see how it changes what you can see when looking at the router settings. This helped me understand how to protect passwords and why encryption is important.Learning these setup tasks is a key building block for working with larger systems and keeping networks secure.



### LAB INSTRUCTIONS
1. Connect R1 and R2 by their GigabitEthernet0/0 interfaces.

2. Set the hostnames according to the network diagram (R1 and R2).

3. Set the enable password on each router to cisco.

4. View the password in the running configuration. Is it encrypted?

5. Enable password encryption on each router.

6. View the password in the running configuration. Is it encrypted?

7. Disable password encryption on each router.

8. View the password in the running configuration. Is it encrypted?


### Tools  
* Cisco Packet Tracer – Used to simulate and configure network devices in a virtual lab environment

* Command-Line Interface (CLI) – Used to enter commands for configuring routers and switches

* Routers – Basic network components used to test and apply configurations

###  Skills Learned
* Learned how to set hostnames to identify devices on a network

* Assigned IP addresses to network interfaces for communication

* Enabled interfaces (turned on device ports) to establish basic connectivity

* Practiced using the CLI (Command-Line Interface) to enter configuration commands

* Gained foundational knowledge for setting up and verifying small network environments


### Lab Instructions for 1 and 2

The first goal of this lab was to connect router 1 and router 2 by their Gigabitethernet0/0 interfaces. Essentality, routers are devices that help connect networks. Routers can forward data from one network to another based on Ip address. They are the gateway of the network. 

![image](https://github.com/user-attachments/assets/7928c638-7f77-40ef-ba73-649b083aebfd)               

![image](https://github.com/user-attachments/assets/d4d9a884-6ad9-4c31-aa2c-e30871920877)


I connected the two routers with a standard network cable (called a straight-through cable) using the ports labeled GigabitEthernet0/0. GigabitEthernet is a very high-speed port on the router used for network connections.

I used the hostname command in global configuration mode to name my routerS "R1"  and "R2" for easy identification in the network setup. 
I utilized these commands below in the screenshot  to complete the step. 



![image](https://github.com/user-attachments/assets/57d969c4-b91c-4434-9ecd-534b416d1499)     
           ![image](https://github.com/user-attachments/assets/9e38ade0-60e5-4547-935d-df4d1275f19b)


**Troubleshooting Tip**

While working on this lab, I noticed I couldn’t run certain commands after entering configuration mode. The fix was simple but is important to remember. 
I first had to type the enable command to enter privileged EXEC mode (also known as enable mode). Only then could I access global configuration mode with configure terminal.
This step is like unlocking "Admin access" before making deep changes to the router. Without it, the router will block certain commands to protect itself.

 Quick Command Flow:
 
Router> enable

Router# configure terminal

Router(config)#

  ### Lab Instruction 3 

Next, I learned how to set up passwords for each router. I entered global configuration mode to set a password using the enable password cisco command for Router 1. Then, I set the password network for the second router as well.



 ![image](https://github.com/user-attachments/assets/89cac745-0639-4e91-b414-ed8187eae2d8)   ![image](https://github.com/user-attachments/assets/5b6d2cb8-6d8f-442a-93e2-b0bbb4e84400)      

![image](https://github.com/user-attachments/assets/d9defb02-ae8a-4a34-bdce-50392e002ab2)     ![image](https://github.com/user-attachments/assets/514b94b8-eb10-40c3-93a7-bacd23cd5669)

### Protecting Your Network: The Role of Router Passwords
Setting passwords on routers is important for network security. Without a password, any one could access the router’s configuration settings and make changes.
Additionally, Attackers often look for open, unsecured devices on a network. A router without a password is an easy entry point for network hijacking, man-in-the-middle attacks, denial-of-service (DoS) attacks.


### Troubleshooting Tip
After setting the enable password network, I wasn’t prompted to enter the password when I typed enable again. This is because I was still in Privileged EXEC mode (R2#).
To test the password prompt, I had to type exit twice to return to User EXEC mode (R2>), then re-enter enable. Once I did that, the router correctly prompted me for the password.




### Lab instruction 4 

For step four of the lab, I navigated to the current configuration of the router to anaylze if the router's password is encrypted. 
 I ran the show runnng commmand *#do sh run* from global configuration mode below in the screenshot.I saw the password cisco was not encrypted      
 

![image](https://github.com/user-attachments/assets/1356c7f0-31bc-4094-aeb2-cb84fd7fe61d)    
**Before Encryption for R1**



![image](https://github.com/user-attachments/assets/5bb6230d-3170-4b7f-a85c-c0b469e7f9ed)

**Before Encryption for R2**

Running the command #do sh run allowed me to view the router’s current settings.
This includes: Hostname, Interface settings (like IP addresses), Routing protocols, Passwords (if not encrypted), VLAN configurations.
I saw the hostname and password were enabled.Additionally, the service password-encryption command was not enabled in the *before encryption for r2* screenshot (based on password visibility)
This command helps confirm if the changes I made in configuration mode are active.Not every change is immediately obvious unless verified. Using show running-config gave me confidence that my settings were correct before testing further.



### Lab instructions 5 and Lab Instructions 6
In order to complete the necessary steps to encyrpt the password . I typed R1 (config) #service password-encryption as shown in the screenshot below 

 
 
![image](https://github.com/user-attachments/assets/58d63f1f-a35f-4b96-95c4-e5049b13a4c4)      
**After Encryption for R1**             



I completed the same exact steps for router 2 as well.
show running command *do sh run* from global configuration mode for router 2 as well. 

![image](https://github.com/user-attachments/assets/3869ec2a-5ef7-4e1b-888a-e272cd2d632f)


**After Encryption for R2**    


Now, each router password is encrypted. We can view this in the router settings in the top screenshot 
 
Lab 5 and Lab 6 have been successfully completed according to the provided instructions.

### The purpose of encrypted passwords in cisco 
Once I encrypt the password Cisco for router 1 and password network for router 2.  it transformed the original password into an unreadable format.
This prevents anyone who views the router’s configuration from seeing the actual password.
Also,it adds a layer of protection, making it harder for attackers to guess or steal the password. 


### Lab InstructionS 7 and Lab Instructions 8
In this section of the lab, I inserted the commands below to disable password encyption. 

R1>enable

Password: 

R1#configure terminal

Enter configuration commands, one per line.  End with CNTL/Z.

R1(config)#no service password-encryption

R1(config)#

![image](https://github.com/user-attachments/assets/7c4ce453-f1c9-45e9-9653-80e17c326f06)

After completing the command  *#no service running config*, I reviewed the router settings after disabling encryption. I noticed that the passwords previously set on each individual router remained encrypted, meaning disabling the encryption only applies to new passwords going forward — it does not decrypt existing ones.

lab 7 and Lab 8 have been successfully completed according to the provided instructions.


 What I Learned in this lab
I learned how to navigate between different user modes in Cisco IOS, including user EXEC, privileged EXEC (enable mode), and global configuration mode. This helped unlock deeper access levels on the router so I could make important changes. 

I now understand the importance of using the enable command to gain higher-level access before configuring the router.

I practiced entering and exiting configuration modes using commands like enable, configure terminal,show running-config,service password-encryption and exit.


I became more familiar with basic router command-line navigation, which is essential for network setup and troubleshooting.

I gained hands-on experience in identifying and resolving permission-related errors when working with router commands.


### COMMANDS SECTION

enable
configure terminal



- Used `enable` to enter **privileged EXEC mode**, which allows advanced commands.
- Entered **global configuration mode** with `configure terminal` to make changes to the router.


The command show running-config (or show run for short) lets you peek at all the current router settings while you're still inside the configuration mode. It’s like checking your notes while you're still writing them — super helpful to make sure you're doing things right.

.

![image](https://github.com/user-attachments/assets/c41408d3-3adf-4729-bf75-30a60a76258c)


## Cisco IOS Modes Breakdown



## 🔑 Cisco IOS Modes Breakdown (R1 and R2)

| Prompt (R1 / R2)          | Mode Name                    | What You Can Do                                                 | Explanation You Can Use Out Loud                                      |
|---------------------------|------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| `R1>` / `R2>`             | User EXEC Mode               | Basic, view-only access (can't make changes)                     | "This is like being a guest — I can look, but I can't touch anything." |
| `R1#` / `R2#`             | Privileged EXEC Mode         | Full read access and some powerful commands like `show run`      | "I used `enable` to unlock higher access and view system configs."     |
| `R1(config)#` / `R2(config)#` | Global Configuration Mode    | Make system-wide changes to the router                           | "I entered `configure terminal` to start changing router settings."    |



 Key Configuration Commands
🔹 Enter Configuration Mode
bash
CopyEdit
enable
configure terminal

🔹 Set Router Hostname
bash
CopyEdit
hostname R1

🔐 Console Access Password
bash
CopyEdit
line console 0
password cisco
login
exit

🔐 VTY Line Password (Telnet/SSH)
bash
CopyEdit
line vty 0 4
password cisco
login
exit

🔐 Enable Passwords
bash
CopyEdit
enable password cisco         
enable secret class            

🔐 Encrypt All Passwords
bash
CopyEdit
service password-encryption

📛 Set Login Banner
bash
CopyEdit
banner motd #Unauthorized access is prohibited#

🌐 Assign IP Address & Activate Interface
bash
CopyEdit
interface gigabitEthernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit


✅ Verification Commands
bash
CopyEdit
show ip interface brief
show running-config


💾 Save the Configuration
bash
CopyEdit
copy running-config startup-config




