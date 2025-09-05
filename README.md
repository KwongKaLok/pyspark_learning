# Installation
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
##
