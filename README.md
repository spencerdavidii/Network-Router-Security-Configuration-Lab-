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



The first goal of this lab was to connect router 1 and router 2 by their Gigabitethernet0/0 interfaces. I used the hostname command in global configuration mode to name my routerS "R1"  and "R2" for easy identification in the network setup. 
I utilized these commands below in the screenshot  to complete the step. 


![image](https://github.com/user-attachments/assets/57d969c4-b91c-4434-9ecd-534b416d1499)

**Commands Utitlized To Change Hostnames**

Essentality, routers are devices that help connect networks. Routers can forward data from one network to another based on Ip address. They are the gateway of the network. 

![image](https://github.com/user-attachments/assets/7928c638-7f77-40ef-ba73-649b083aebfd)

I connected the two routers with a standard network cable (called a straight-through cable) using the ports labeled GigabitEthernet0/0.GigabitEthernet is a very high-speed port on the router used for network connections.

  ![image](https://github.com/user-attachments/assets/d4d9a884-6ad9-4c31-aa2c-e30871920877)


Router> enable
Router# configure terminal
Router(config)# hostname R1
