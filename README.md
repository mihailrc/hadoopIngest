# Hadoop Ingest

## From local file system

### Ingesting files using the command line

**Note** if copying files from a client to a Hadoop cluster make sure that Hadoop versions are compatible. For example Hadoop 1 on the client and Hadoop 2 on the cluster will fail. Also make sure that the client can communicate both with the Name Node **and** the Data Nodes. If you can create directories but nor copy files probably either the Data Nodes are full or you cannot communicate with them.

```
#create a testing directory
hadoop fs -mkdir -p hdfs://127.0.0.1/testing/files
hadoop fs -copyFromLocal README.md hdfs://127.0.0.1/testing/files
#remove the testing directory
hadoop fs -rm -r hdfs://127.0.0.1/testing 
```

Provide examples using the following mechanisms:
 - HDFS Java API
 - WebHDFS Rest API 

TODO
Discuss about:
 - libraries that simplify ingestion: Pail
 - consider access patterns when organizing files in HDFS
 - security
