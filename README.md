# Azure-Virtual-Network
The files included in this repository was used to configure the network as shown below:

![diagram](https://user-images.githubusercontent.com/31974326/148467888-cc4f48ef-b969-4fde-a63b-3ab338a0d6d7.PNG)

These files were tested and deployed on Microsoft Azure. Although the files altogether create the deployment depicted above, they can independently function and install piece by piece, by separating components such as Filebeat or Kibana.

## Topology

The ELK server allows users to easily monitor and track the VMs on the network. Filebeat monitors, collects, and forwards log files while Metricbeats does the same for OS metrics. Kibana takes the information forwarded to the ELK server and provides data visualization and log analytics to the user.

## ELK Configuration

The ELK machine was configured using an automated Ansible playbook. This allows for simple distribution of this specific configuration as it can be deployed to other machines with a single command rather than manually configuring each VM 1 at a time. 

https://github.com/ttoyokawa/Azure-Virtual-Network/blob/main/Images/docker-ps.PNG

The above image shows the result of running the command docker ps after the playbook is successfully executed.

## How to use the playbook

Assuming an Ansible control node is already provisioned:

Access the control node
*Copy the config file into the Ansible container.
*Update the hosts file to include the IPs of hosts to be configured. 
*Run the playbook and navigate to the ELK-VM's public IP on port 5601 to confirm the installation. 
