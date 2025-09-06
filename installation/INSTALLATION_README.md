# Installation (Master & Worker Node)
## 1. Check Java version
```
java -version
```
Output:
```
openjdk version "17.0.16" 2025-07-15
OpenJDK Runtime Environment (build 17.0.16+8-Ubuntu-0ubuntu122.04.1)
OpenJDK 64-Bit Server VM (build 17.0.16+8-Ubuntu-0ubuntu122.04.1, mixed mode, sharing)
```
### (Optional) 1.1 Install Java 17
```
sudo apt install openjdk-17-jdk
```
### (Optional) 1.2 Switch Java version
List all java versions:
```
update-java-alternatives --list
```
Switch java version:
```
sudo update-java-alternatives --set /usr/lib/jvm/java-1.17.0-openjdk-amd64
```
## 2. Download Apache Spark
```
wget https://dlcdn.apache.org/spark/spark-4.0.0/spark-4.0.0-bin-hadoop3.tgz
```
# Setup
## Set Up the Installation Directory
```
mkdir ~/spark
mv spark-4.0.0-bin-hadoop3.tgz ~/spark/
cd ~/spark
```
## Extract the downloaded Spark file
```
tar -xvzf spark-4.0.0-bin-hadoop3.tgz
```
## Set up the Spark Path
Edit the ~/.bashrc file, add these lines
```
export SPARK_HOME=/home/kwongkalok/spark/spark-4.0.0-bin-hadoop3
export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/bin
export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin
```
## Validate Apache Spark Runs Locally
```
$ spark-shell
WARNING: Using incubator modules: jdk.incubator.vector
Using Spark's default log4j profile: org/apache/spark/log4j2-defaults.properties
25/09/06 16:07:07 WARN Utils: Your hostname, node0, resolves to a loopback address: 127.0.1.1; using 192.168.128.54 instead (on interface enp0s1)
25/09/06 16:07:08 WARN Utils: Set SPARK_LOCAL_IP if you need to bind to another address
Using Spark's default log4j profile: org/apache/spark/log4j2-defaults.properties
Setting default log level to "WARN".
To adjust logging level use sc.setLogLevel(newLevel). For SparkR, use setLogLevel(newLevel).
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 4.0.0
      /_/
         
Using Scala version 2.13.16 (OpenJDK 64-Bit Server VM, Java 17.0.16)
Type in expressions to have them evaluated.
Type :help for more information.
25/09/06 16:07:12 WARN NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Spark context Web UI available at http://192.168.128.54:4040
Spark context available as 'sc' (master = local[*], app id = local-1757146033107).
Spark session available as 'spark'.

scala> 
```
