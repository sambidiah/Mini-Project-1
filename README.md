## Mini-Project-1
Mini Project 1 - Creating and describing a Network for Cloud Computing

## Step by Step Config
- Objectives

The objective of this project was to create a sample Network that showed the AIMS/ISBA Lab and how it is connected to the Datacenter for the Business College

- Use Cases for This System

1) The first use case would be for a Network administator to better understand how everything is connected together between the lab and the datacenter if they have to troubleshoot or make a new addition to the system
2) The second use case would be that this system now has a design for a Network Administrator to recreate it. Should there be another lab (such as the bloomberg lab) they would be able to understand the necessary links quicker than if they did not have a framework
3) Educational Environments - This framework can be used in class rooms to either set up a basic network or teach students how to set up a basic one
4) Small Businesses - This framework provides a step by step guide on how to create and connect two separate lans together for business owners who might not have a lot of experience in this field

### Detailed Step by Step Set up

1) Software and hardware Requirements for the entire project

*Hardware*
- Cisco Router (1)
- Cisco switches (2)
- Ethernet cables (6)
- Laptops (4)

*Software*
- Cisco Packet tracer - for simulation
- Webserver Software (MAMP)
- DNS server software (NAMO)

2) Creating a LAN - IP Address set up

*Objective of this step* - Create two distinct Private IP Addresses to use later on

- When creating a LAN, you will have to create unique IP Addresses within the subnet range that we define. For LAN 1 we will be using 192.168.0.0/26 and for LAN 2 172.16.0.0/24. The first step in this process is determining the Subnet Range and available IP Range (below)
*LAN 1*
- SUBNET MASTK - 255.255.255.192
- Available IP Range - 192.168.0.2 to 192.168.0.62 (192.168.0.1 is reserved for the router AKA the default gateway)

*LAN 2*
- SUBNET MASTK - 255.255.255.0
- Available IP Range - 172.16.0.2 to 172.16.0.254 (172.16.0.1 is reserved for the router AKA the default gateway)

*Assigning Static IP Addresses (On MAC)*
- Go to System Preferences > Network
- Turn off Wifi and Select Ethernet
- Click Advanced > TCP/IP
- Set configure IPv4 to Manually
- **IP Address** Manually input the nextmost available IP in the Range of the LAN that you are using
- **Subnet Mask** Manually input the subnet mark for the LAN you are using
- **Router** (CHECK THIS) Enter the first (0.1) IP address for the router interface

3) Connect devices to switch and make sure they can communicate

*Objective of this step* - Confirm that you are able to commincate with devices on your LAN

- First, you have to make sure you have the proper hardware ready and connected
  -This includes the Switch, two Mac computers, and then 2 Ethernet cables
- Second, you have to physically connect the computers to the switch
  - Get the Cisco Switch and set it in between two of the different LANS (make sure these computers are on the same LAN)
  - Plug the Cisco switch into a power outlet and make sure that it is on
  - Plug one end of the Ethernet Cable into the Ethernet port of your computer
  - Plug the other end into any available port on the switch (ideally make sure they are in order)
    - Repeat this for any following device that needs to be connected to the LAN   

4) Set up a WebServer

5) Set up a DNS

6) Make sure that you can access the webpage through the domain name

7) Connect to the router

8) Communicate ith the other lan


## FAQ


## Retrospective
