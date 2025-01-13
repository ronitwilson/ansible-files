ansible webservers -m ping
ansible-playbook tomcat-10-playbook.yml
ansible-playbook tomcat-10-playbook.yml -e tomcat_user=tomcat -e tomcat_password=password

# Ansible roles
Precreated roles
https://galaxy.ansible.com/ui/standalone/roles/?page=2&page_size=10&sort=-created 

```
ansible-galaxy init tomcat
ansible-galaxy init java
```
* helps in reuseablility

we can place the commands in tasks/main.yml

user roles in the main.yml

## Using generic playbooks
```
    - name: qqq
      apt:
       update_cache: yes
      when: ansible_facts['ansible_distribution'] == "Ubuntu"
```
another example ``` when: ansible_facts['ansible_distribution'] == "Ubuntu" ``` 
also ``` when: OS == "Ubuntu" ```where os can be set as environment variable with "-e"
