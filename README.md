## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Diagram of the Network](images/proj-1_network-diagram.jpg)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

The playbook implements the following tasks:
---
- name: Configure Elk VM with Docker
  hosts: elkserver
  become: true
  tasks:

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.
- Load balancing ensures that the application will be highly available, in addition to restricting access to the network.
- The primary function of a load balancer is to spread workloads across multiple servers to prevent overloading servers, optimize productivity, and maximize uptime. Load balancers also add resiliency by rerouting live traffic from one server to another if a server falls prey to DDoS attacks or otherwise becomes unavailable. In this way, load balancers help to eliminate single points of failure, reduce the attack surface, and make it harder to exhaust resources and saturate links.
-  What is the advantage of a jump box? A jumpbox, when configured correctly, creates a single point of entry into your network. When ssh key is used to establish connection between host and jumpbox, and private ip's are used for other vm's on network and all connections are then forced through jumpbox, the attack surface is greatly reduced.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the data and system logs.
- Filebeat will collect log events and gather data about the file system.
- Metricbeat will be used to monitor and collect metrics from the system and services running on each server.

The configuration details of each machine may be found below.
_
|         Name         |                  Function                 |   IP Address  |     Operating System    
|:--------------------:|:-----------------------------------------:|:-------------:|:-----------------------:|
| Jump Box Provisioner | Gateway                                   | 10.0.0.4      | Linux Ubuntu 18.04-LTS  |   
| Local Workstation    | Configurating network externally          | 98.233.82.210 | Windows 10 Pro Edition  |   
| Web-1 VM             | Process and deliver web content to user   | 10.0.0.5      | Linux Ubuntu 18.04-LTS  |   
| Web-2 VM             | Process and deliver web content to user   | 10.0.0.7      | Linux Ubuntu 18.04-LTS  |   
| ELK-Server           | Collect and process data from Web VMs     | 10.2.0.4      | Linux Ubuntu 18.04-LTS  |   
| Load Balancer        | Distribute Traffic to backend server pool | 20.119.114.243| N/A                     |   

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the jump-box(gateway) machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 98.233.82.210

Machines within the network can only be accessed by jump box provisioner.
- 10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | No                  | 98.233.82.210        |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

