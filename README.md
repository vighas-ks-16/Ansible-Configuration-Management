# Ansible-Configuration-Management
Configuration Management of Servers using Ansible


💻🔧 Throughout this journey, I've immersed myself in Ansible playbooks, ad-hoc commands, and Ansible Galaxy, unveiling boundless automation potentials. Here's a glimpse of my insights and how I've revolutionized my project:

### Mastering Ansible Playbooks: 
The configuration management process has never been smoother! Ansible playbooks, with the YAML structure, helps to define tasks, roles, and configurations, ensuring seamless deployment across diverse servers.

### Harnessing Ansible Ad-hoc Commands: 
Ansible's ad-hoc commands have been a game-changer for swift tasks and troubleshooting. With concise commands, we can execute actions across the infrastructure, from basic system checks to intricate updates.

### Unlocking Ansible Galaxy: 
Embracing Ansible Galaxy has turbocharged the operations. This treasure trove of Ansible roles provides ready-made solutions, expediting the deployment process and upholding top-notch configuration management practices.

### Project Integration: 
Ansible stands as the linchpin of the configuration management strategy. From provisioning new servers to orchestrating software installations and updates, Ansible automates repetitive tasks, minimizes errors, and amplifies efficiency.

### PROJECT WORKFLOW :

Prerequisite :

We need two servers. The Server in which Ansible is installed is called as the Ansible Server. 

![image](https://github.com/vighas-ks-16/Ansible-Configuration-Management/assets/107311113/3f599c6b-a22e-475e-afa4-ef6c52ea87cd)

![image](https://github.com/vighas-ks-16/Ansible-Configuration-Management/assets/107311113/2bad6887-f41c-4513-a606-ba0df4826fe9)



Aim :

Ansible Server should be able to communicate with the other server (Target Server) without any password.

Ansible Playbook :

Ansible files having multiple commands.

Highly reusable.

Ansible adhoc commands :

They are quick commands to run with Ansible without writing an Ansible Playbook.

Not reusable.

Inventory file :

Stores the IP Address of Target Servers.

The below command will be executed on all the hosts which are listed in the Inventory file :

```
ansible -i inventory all -m "shell" -a "touch devopsclass"
```

There are two different types of servers :

1. dbservers
   
2. webservers

Open the Inventory file and do the grouping of the servers.

If you want to execute the ansible commands only on the webservers, use :

```
ansible -i inventory webservers -m "shell" -a "df"
```

![image](https://github.com/vighas-ks-16/Ansible-Configuration-Management/assets/107311113/35312845-61cf-4dbf-9435-2abfa842f75e)

![image](https://github.com/vighas-ks-16/Ansible-Configuration-Management/assets/107311113/4c1477fd-3502-4edc-ae15-17b945667168)

![image](https://github.com/vighas-ks-16/Ansible-Configuration-Management/assets/107311113/a776eb61-167f-4979-b29e-e8bf2e8bd844)





Running the ansible playbook :

```
ansible-playbook -vvv -i inventory first-playbook.yml
```

![image](https://github.com/vighas-ks-16/Ansible-Configuration-Management/assets/107311113/647b2f5b-8f86-4f90-b76f-e3e7e7ed3f4e)



