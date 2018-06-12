# elastic-search

Install Elasticsearch on Cent OS 7

## System Config: vCPU:2(minimum) Ram:4Gb(minimum)

VM on GCP

Elasticsearch requires Java 8, an open-source distribution such as [OpenJDK.](https://www.server-world.info/en/note?os=CentOS_7&p=jdk8&f=2)

```
sudo yum -y install java-1.8.0-openjdk java-1.8.0-openjdk-devel
```

```
java -version
```

```
sudo yum -y install wget
```

Download Elasticsearch RPM

```
 wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.2.4.rpm
 
 sudo rpm --install elasticsearch-6.2.4.rpm
```

configure Elasticsearch

```
sudo chkconfig --add elasticsearch
```

Start using the service command:

```
sudo -i service elasticsearch start
```

You can test that your Elasticsearch node is running by sending an HTTP request to port 9200 on localhost:

```
curl -X GET "localhost:9200/"
```

Stop using the service command:

```
sudo -i service elasticsearch stop
```

