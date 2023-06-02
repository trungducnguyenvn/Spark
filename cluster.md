## Spark Cluster with Standalone Mode
To create a Spark cluster in Standalone Mode so that the cluster can remain running even after we stop running our notebooks.

- Spark install directory from a terminal and run the following command:
```
./sbin/start-master.sh
```

- Then run the following command to start a worker node:
```
./sbin/start-slave.sh spark://<URL>:7077
```

- If you want to run multiple worker nodes, you can run the following command:
```
./sbin/start-slave.sh spark://<URL>:7077 -c <number of cores> -m <memory per node> -p <port> 
```

- Create a SparkSession object in Notebook/ Python code to connect to the cluster:
```
spark = SparkSession.builder \
    .master("spark://<URL>:7077") \
    .appName('test') \
    .getOrCreate()
```

` Note: Replace <URL> with the URL of your master node.`

- To stop the cluster, run the following command:
```
./sbin/stop-all.sh
```







