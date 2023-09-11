# Installation Oracle Database XE 21c in Centos7

### Create directory Oracle
    mkdir /opt/oracle
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/498910d0-e67e-413b-9c77-0b7041e30023)

### Use sudo to log in as root.
    sudo -s
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/ba57cfcb-e05b-4b47-ab68-9ace938f07fb)

Use yum to install wget command

    sudo yum install wget

### Download Oracle repository Database and preinstall 
    wget https://download.oracle.com/otn-pub/otn_software/db-express/oracle-database-xe-21c-1.0-1.ol7.x86_64.rpm
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/c4dbf908-d6b3-4c32-ba07-ab7eb7cd01ab)

    wget https://yum.oracle.com/repo/OracleLinux/OL7/latest/x86_64/getPackage/oracle-database-preinstall-21c-1.0-1.el7.x86_64.rpm
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/7eb6e9be-2b23-435b-9e4a-98609c803d86)

### Run the Oracle Database Preinstallation RPM
    yum -y localinstall oracle-database-preinstall-21c-1.0-1.el7.x86_64.rpm
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/bea3761c-ef9a-4991-97bf-931d52560b96)

### Install the database software
    yum -y localinstall oracle-database-xe-21c-1.0-1.ol7.x86_64.rpm
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/349f282f-0690-40ae-b023-eba5ca627542)

### If the install cannot proceed
![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/78672f40-2fdf-478b-b485-b9a5d3172e81)

Running this command and retry the installation.

    sudo chown -R oracle:oinstall /opt/oracle # this is a prerequisite from Oracle, there is no workaround for that

Note: softlink will not provide full access and\or ownership on the original directory

### Creating and configuring Oracle Database
Create the database by running the configure operation. When prmpted, provide the passwords for SYS, SYSTEM and PDBADMIN users. This takes a few minustes to complete.

    /etc/init.d/oracle-xe-21c configure

![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/a257df09-0539-43eb-8ad5-ae8231553b9c)

This completes Oracle Database 21c XE installation and configuration. It is recommended to setup the environment variables before starting to use Oracle Database XE.

![image](https://github.com/arliputraa/installation-oracle-database-21c-xe-centos7/assets/110078907/be809f84-36e1-427a-97a6-3df329c2ba00)



