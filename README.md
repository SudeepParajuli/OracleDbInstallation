# oracledb-ansible
Ansible playbook to configure a CentOS/RHEL/Oracle Linux 7 server with Oracle 12c R1 Enterprise Edition Database

Requirement : 

- Ansible
- Centos 7 as a deployment server  


Download from Oracle support the Oracle installation files: 
- linuxamd64_12102_database_1of2.zip
- linuxamd64_12102_database_1of2.zip
and put them to folder roles/oracle-install/files inside checkout folder

Further put the private key ( key from which server has been created ) file inside the ansible.cfg file  and the deployment server ip inside host file in ansible source code . 

Once the file has been kept in respective folder . Run the following command from Ansible master . 

```
ansible-playbook -i hosts oracle-db.yml -e ansible_python_interpreter=auto -v

```

After a few minutes a virtual centos machine  with Oracle Database will be ready for you without any further configuration. You can access the Enterprise Manager Express using sys/sysdba and “oracle” as password.

https://oradb3.private:5500/em


password for Oracle Operating system user is welcome1


