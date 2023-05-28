# Web infrastructure design

**Web infrastructure design** is the process of planning and implementing the hardware, software, and networking components that make up a website.<br /> The goal of web infrastructure design is to create a system that is reliable, scalable, and secure.


There are a number of factors to consider when designing a web infrastructure, including:

The size and complexity of the website
The expected traffic levels
The budget
The security requirements
Once the factors have been considered, the next step is to select the appropriate hardware and software. The hardware will typically include servers, storage devices, and networking equipment. The software will include the operating system, web server, database server, and application server.

Once the hardware and software have been selected, the next step is to configure the system. This includes tasks such as setting up the operating system, installing the software, and configuring the network.

Once the system is configured, the next step is to test it. This includes testing the performance, reliability, and security of the system.

Once the system has been tested, it is ready to be deployed. This includes tasks such as making the website available to users and monitoring the system for performance and security issues.

Web infrastructure design is a complex process, but it is essential for ensuring the success of a website. By carefully considering the factors involved and selecting the appropriate hardware, software, and configuration, it is possible to create a system that is reliable, scalable, and secure.

### Here are some additional tips for designing a web infrastructure:

**Use a scalable architecture.**<br /> This will allow you to easily add capacity as your website grows.
**Use reliable hardware and software.**<br /> This will help to ensure that your website is always available to users.
**Implement security measures.**<br /> This will help to protect your website from attack.
**Monitor your system.**<br > This will help you to identify and fix problems before they impact your users.<br />
By following these tips, you can design a web infrastructure that will help you to achieve your business goals.

### 0. Simple web stack
mandatory
A lot of websites are powered by simple web infrastructure, a lot of time it is composed of a single server with a LAMP stack.

On a whiteboard, design a one server web infrastructure that hosts the website that is reachable via www.foobar.com. Start your explanation by having a user wanting to access your website.

### Requirements:

**You must use:**
1 server
1 web server (Nginx)
1 application server
1 application files (your code base)
1 database (MySQL)
1 domain name foobar.com configured with a www record that points to your server IP 8.8.8.8
**You must be able to explain some specifics about this infrastructure:**
What is a server
What is the role of the domain name
What type of DNS record www is in www.foobar.com
What is the role of the web server
What is the role of the application server
What is the role of the database
What is the server using to communicate with the computer of the user requesting the website
You must be able to explain what the issues are with this infrastructure:
SPOF
Downtime when maintenance needed (like deploying new code web server needs to be restarted)
Cannot scale if too much incoming traffic
Please, remember that everything must be written in English to further your technical ability in a variety of settings.

### 1. Distributed web infrastructure
mandatory
On a whiteboard, design a three server web infrastructure that hosts the website www.foobar.com.

## Requirements:

**You must add:**
2 servers
1 web server (Nginx)
1 application server
1 load-balancer (HAproxy)
1 set of application files (your code base)
1 database (MySQL)
You must be able to explain some specifics about this infrastructure:
For every additional element, why you are adding it
What distribution algorithm your load balancer is configured with and how it works
Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both
How a database Primary-Replica (Master-Slave) cluster works
What is the difference between the Primary node and the Replica node in regard to the application
You must be able to explain what the issues are with this infrastructure:
Where are SPOF
Security issues (no firewall, no HTTPS)
No monitoring
Please, remember that everything must be written in English to further your technical ability in a variety of settings.

### 2. Secured and monitored web infrastructure
mandatory
On a whiteboard, design a three server web infrastructure that hosts the website www.foobar.com, it must be secured, serve encrypted traffic, and be monitored.

### Requirements:

**You must add:**
3 firewalls
1 SSL certificate to serve www.foobar.com over HTTPS
3 monitoring clients (data collector for Sumologic or other monitoring services)
You must be able to explain some specifics about this infrastructure:
For every additional element, why you are adding it
What are firewalls for
Why is the traffic served over HTTPS
What monitoring is used for
How the monitoring tool is collecting data
Explain what to do if you want to monitor your web server QPS
You must be able to explain what the issues are with this infrastructure:
Why terminating SSL at the load balancer level is an issue
Why having only one MySQL server capable of accepting writes is an issue
Why having servers with all the same components (database, web server and application server) might be a problem
Please, remember that everything must be written in English to further your technical ability in a variety of settings.

### 3. Scale up
#advanced
Readme

### Application server vs web server
### Requirements:

**You must add:**
1 server
1 load-balancer (HAproxy) configured as cluster with the other one
Split components (web server, application server, database) with their own server
You must be able to explain some specifics about this infrastructure:
For every additional element, why you are adding it
Please, remember that everything must be written in English to further your technical ability in a variety of settings.
