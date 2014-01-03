vagrant-hadoop-hive
===================

Create a box which includes
* OpenJDK 1.7
* Apache Hadoop 1.2.1
* Apache Hive 0.11.0

Use
===
Required:
* Installed latest Vagrant
* Installed latest Virtual box

Clone this project to local machine and run

    vagrant up

This would up the ubuntu server box and install some packages. Once running is done, you should see the "Good luck!" message, so everything shoud be ready. 

SSH to VM

    vagrant ssh

For starting hadoop without asking the password

	ssh-keygen -t dsa -P '' -f /home/vagrant/.ssh/id_dsa
	cat /home/vagrant/.ssh/id_dsa.pub >> /home/vagrant/.ssh/authorized_keys

Starting Hadoop
	
	start-all.sh
	
Starting Hive

    hive
    
For testing, create a sample table

    hive>CREATE TABLE pokes (foo INT, bar STRING);
    
Access DFS on browser 
[http://dev-hadoop:50070/dfshealth.jsp](http://dev-hadoop:50070/dfshealth.jsp)
    
Access job tracker on browser
[http://dev-hadoop:50030/jobtracker.jsp](http://dev-hadoop:50030/jobtracker.jsp)
    
*NOTEs: dev-hadoop is forwarding to 192.168.33.15 automatic, this is private ip of Virtual machine, you can change in Vagrantfile*
