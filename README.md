## Mini-Project-1
Mini Project 1 - Creating and describing a Network for Cloud Computing

## Step by Step Config
- Objectives

The objective of this project was to create two separate LANS that can communicate across the WAN and with each other

- Use Cases for This System

1) The first use case would be for a Network administator to better understand how everything is connected together between the lab and the datacenter if they have to troubleshoot or make a new addition to the system
2) The second use case would be that this system now has a design for a Network Administrator to recreate it. Should there be another lab (such as the bloomberg lab) they would be able to understand the necessary links quicker than if they did not have a framework
3) Educational Environments - This framework can be used in class rooms to either set up a basic network or teach students how to set up a basic one
4) Small Businesses - This framework provides a step by step guide on how to create and connect two separate lans together for business owners who might not have a lot of experience in this field

### Detailed Step by Step Set up

1) Software and hardware Requirements for the entire project

*Objective of this step* - Making sure that you have all the required hardware and software ready and able to be installed

*Hardware*
- Cisco Router (1)
- Cisco switches (2)
- Ethernet cables (6)
- Laptops (4)

*Software*
- Cisco Packet tracer - for simulation
- Webserver Software (MAMP)
- DNS server software (NAMO)

2) Connect devices to switch

*Objective of this step* - Confirm that you are able to commincate with devices on your LAN

- First, you have to make sure you have the proper hardware ready and connected
  -This includes the Switch, two Mac computers, and then 2 Ethernet cables
- Second, you have to physically connect the computers to the switch
  - Get the Cisco Switch and set it in between two of the different LANS (make sure these computers are on the same LAN)
  - Plug the Cisco switch into a power outlet and make sure that it is on
  - Plug one end of the Ethernet Cable into the Ethernet port of your computer
  - Plug the other end into any available port on the switch (ideally make sure they are in order)
    - Repeat this for any following device that needs to be connected to the LAN   

3) Creating a LAN - IP Address set up

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

4) Ensure Communication Across the LAN

*Objective of this step* - Making sure that you can communicate across the individual LANS with the other computer that is a part of it

  - Once all devices are connected to the LAN Physically, you have to test to make sure that these computers can send data back and forth to each other
    - Open terminal on Mac
    - Have one of the computers write this code
      - ping (other computer's new IP address)
    - if the connection is successful, you'll get a reponse from the terminal

**IF IT DOES NOT REPSOND**
  - Check to make sure that ethernet cables are properly connected
  - Check to make sure you inputted the right IP addresses
  - Ensure the switch is turned on 

5) Set up a WebServer

*Objective of this step* - Configuring one laptop to function as the webserver

  - Install MAMP and open it in the application folder
  - Select Nginx as the web server
  - Update the Nginx port from 8888 to 80
    - Preferences > Ports > Nginx Port: 80 > OK
  - Click Start
    - Create index.html in the directory for the Mac operating system
      - /Applications/MAMP/htdocs/index.html
  - Using a text/code editor, replace the index.html with
    - "Welcome to Capstone Consulting ##"

**Trouble Shooting**

  - Disable firewalls
  - Or add a firewall to allow ICMP 

6) Set up a DNS

*Objective of this step* - Create a server that maps domain names to IP Addresses. This way users can access a website by a domain name (I.E. example.com) instead of having to manualy type the IP address

  - Configure and install NAMO (local DNS server)
  - Click + to add a new host
  - Create a host name
    - example.com
  - IPv4: Ip address of the laptop now designated as a DNS server

7) Make sure that you can access the webpage through the domain name

*Objectives of this step* - Make sure that you can access the webpage, both from IP address as well as the domain name 

   - Open a browser and first input the IP address to make sure you can access it through IP (on the webserver)
   - After confirming this, see if you can (on the webserver) type in the domain name that you assigned and make sure you can access this

8) Connect to the router

*Objective of this step* - set the router so that the LANs can communicate with each other

  - The steps for this section of the process are as follows
    - Power on the router > connect the router to both switches (creating the WAN) > add an IP to the router (default gateway)
   
*Hardware needed and how to use it*
  - Conect the router to a power supply
  - Connect ethernet cables from the switch to the router's GigabitEthernet 0/0 for LAN 1
  -  Connect ethernet cables from the switch to the router's GigabitEthernet 0/1 for LAN 2
  -  Ensure the router is powered on and that the switches are connected properly
   
**For MAC Configuration of the Router**

  - Install the driver for Serial Adapter
  - Open terminal and 

9) Communicate with the other LAN

*Objectives of this steps* - Test communication and make sure everything is set up correctly

  - First, using a computer in LAN 1, try to ping a computer in LAN 2
  - If you can ping them, using LAN 2, try to access the webpage (using domain name) that LAN 1 set up
  - If you can do this step, then congrats! you've finished
  - If you have not, please review the steps (primarily step 8)

## FAQ

  1) Unable to ping between devices
  2) Webpage not loading
  3) No DNS resolution
  4) .
  5) .
  6) .
  7) .
  8) .
  9) .
  10) 

## Retrospective
