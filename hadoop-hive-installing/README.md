About
====

This is a simple script for install Apache Hadoop 1.2.1 and Hive 0.11 on Ubuntu server
This script required JAVA must install on Ubuntu server first and JAVA_HOME must existed already.

Steps
====

#. Setup JAVA and create environment variable JAVA_HOME

    export JAVA_HOME=<path_to_java>
    
#. Move home

    cd ~/
    
#. Clone the scripts from github

    git clone git@github.com:congdang/hadoop-hive-installing.git
    
#. Move to hadoop-hive-installing

    cd hadoop-hive-installing
    
#. Set execute permision for script

    sudo chmod +x install.sh
    
#. Run script for installing

    ./install.sh
    
*Once the script is finished then Hadoop be ON and Hive is ready for using*

For testing, you can access on browser
*Modify hosts file on your local*
        ip-of-hadoop-machine  myhadoop
        
http://myhadoop:50070 to see the NameNode status 
http://myhadoop:50030 to see the MapReduce status.

Using Hive
==========

#. start hive

    hive
    
#. Create a sample table

    hive> CREATE TABLE pokes (foo INT, bar STRING);
    
#. Listing the Hive warehouse

    $HADOOP_HOME/bin/hadoop dfs -ls /user/hive/warehouse







    

    

  



