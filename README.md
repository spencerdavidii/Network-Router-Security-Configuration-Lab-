# Network-Router-Security-Configuration-Lab-

### OBJECTIVE
The goal of this lab was to get comfortable setting up network equipment like routers and switches from scratch. II learned how to name the devices,assign ip addresses, turn on their ports, and give them the right digital addresses so they can talk to each other. This helped me understand the basic steps needed to power network device online and ensure basic connectivity . Learning these setup tasks is a key building block for working with larger systems and keeping networks secure.

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

* PCs, Switch, and Router (virtual) – Basic network components used to test and apply configurations

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




  ### Lab Instruction 3 

Next, I learned how to set up passwords for each router to connect to cisco. I entered global configuration mode to set a password using the enable password cisco command, which helps secure access to the router's privileged mode.
Then, I set the password network for the second router as well.


 ![image](https://github.com/user-attachments/assets/89cac745-0639-4e91-b414-ed8187eae2d8)   ![image](https://github.com/user-attachments/assets/5b6d2cb8-6d8f-442a-93e2-b0bbb4e84400)      

![image](https://github.com/user-attachments/assets/d9defb02-ae8a-4a34-bdce-50392e002ab2)     ![image](https://github.com/user-attachments/assets/514b94b8-eb10-40c3-93a7-bacd23cd5669)

### Protecting Your Network: The Role of Router Passwords
Setting passwords on routers is important for network security. Without a password, any one could access the router’s configuration settings and make changes.
Additionally, Attackers often look for open, unsecured devices on a network. A router without a password is an easy entry point for network hijacking, man-in-the-middle attacks, denial-of-service (DoS) attacks.


### Lab instruction 4 

For step four of the lab, I went to view  the password for R1 in the running configuration. The objective was to identify is the password encrypted. 
I saw the password cisco was not encyrpted. So I ran the commmands *#do sh run* from global configuration mode Privileged EXEC  mode below in the screenshot. 
The show running command can aabbreviated as sh run 

![image](https://github.com/user-attachments/assets/58d63f1f-a35f-4b96-95c4-e5049b13a4c4)
    ![image](https://github.com/user-attachments/assets/1356c7f0-31bc-4094-aeb2-cb84fd7fe61d)   
                                                                                           


I completed the same commands for router 2 as well. 

![image](https://github.com/user-attachments/assets/3869ec2a-5ef7-4e1b-888a-e272cd2d632f)
















