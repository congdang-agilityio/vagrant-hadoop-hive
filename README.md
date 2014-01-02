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

This would up the ubuntu server box and install some packages. Once running is done, you should see the "Good luck!" message, so everything shoud be ready. SSH to VM to work with Hive

    vagrant ssh

Starting Hive

    hive
    
Access DFS on browser 
[http://192.168.33.15:50070/dfshealth.jsp](http://192.168.33.15:50070/dfshealth.jsp)
    
Access job tracker on browser
[http://192.168.33.15:50030/jobtracker.jsp](http://192.168.33.15:50030/jobtracker.jsp)
    
*NOTEs: 192.168.33.15 is private ip of Virtual machine*
