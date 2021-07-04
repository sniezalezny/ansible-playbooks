# ansible-playbooks
This is repo with my firsts ansible-playbooks.



Use playbooks:

paste command to terminal: `ansible-playbook -i hosts.yml -u root ansible-playbooks/NAMEFILE.yml`

example:`ansible-playbook -i hosts.yml -u root ansible-playbooks/installpackages.yml`
example:`ansible-playbook -i hosts.yml -u root ansible-playbooks/update-upgrade.yml`

If You want simple-test connection with your serwers, You can use:

ansible -i hosts.yml all -u root -k -m ping 

example hosts.yml file:


`all:
  children:
    default:
      hosts:
        agent1:
          ansible_port: 8822
          ansible_user: root
        agent2:
          ansible_port: 8823
          ansible_user: root
        agent3:
          ansible_port: 8824
          ansible_user: root
      vars:
        ansible_python_interpreter: /usr/bin/python3.5`


