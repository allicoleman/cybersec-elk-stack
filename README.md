## Automated ELK Stack Deployment

This document contains the following details:

Description of the Topology
Access Policies
ELK Configuration
Beats in Use
Machines Being Monitored
How to Use the Ansible Build
Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting in-bound access to the network.

A load balancer intelligently distributes traffic from clients across multiple servers without the clients having to understand how many servers are in use or how they are configured. Because the load balancer sits between the clients and the servers it can enhance the user experience by providing additional security, performance, resilience and simplify scaling your website.
What is the advantage of a jump box?

A jump box is a secure computer that all admins first connect to before launching any administrative task or use as an origination point to connect to other servers or untrusted environments.
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the jumpbox and system network_. -What does Filebeat watch for? Changes to file changes on the machine. -What does Metricbeat record? collect metrics from the operating system and from services running on the server.

The configuration details of each machine may be found below.

Name	Function	IP Address	Operating System
Jump Box	Gateway	40.118.185.100	Linux
Web-1	Webserver	10.1.0.5	Linux
Web-2	Webserver	10.1.0.6	Linux
ELK-Server	Monitoring	10.0.0.4	Linux

Access Policies
The machines on the internal network are not exposed to the public Internet.

Only the jump box provisioner machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

5061 Kibana Port
Machines within the network can only be accessed by jump box provisioner.

Which machine did you allow to access your ELK VM?

My IP Address: 99.122.6.55
A summary of the access policies in place can be found in the table below.

Name	Publicly Accessible	Allowed IP Addresses
Jump Box	Yes	40.118.185.100
Web-1	No	10.1.0.5
Web-2	No	10.1.0.6
ELK-Server	No	10.0.0.4
Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because... What is the main advantage of automating configuration with Ansible?

Free: Ansible is an open-source tool.
Very simple to set up and use: No special coding skills are necessary to use Ansible’s playbooks (more on playbooks later).
Powerful: Ansible lets you model even highly complex IT workflows.
Flexible: You can orchestrate the entire application environment no matter where it’s deployed. You can also customize it based on your needs.
Agentless: You don’t need to install any other software or firewall ports on the client systems you want to automate. You also don’t have to set up a separate management structure.
Efficient: Because you don’t need to install any extra software, there’s more room for application resources on your server.
The playbook implements the following tasks: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc.

Install docker.io
Install pip3
Install Docker python module
Increase virtual memory
Download and launch a docker

