# spark-learn
Project for Learning Batch and Streaming data



## Linux

Install Spark 3.3.2 for Linux-WSL
### Installing Java

Download OpenJDK 11 or Oracle JDK 11 (It's important that the version is 11 - spark requires 8 or 11)

We'll use [OpenJDK](https://jdk.java.net/archive/)

Download it (e.g. to `~/spark`):

```
wget https://download.java.net/java/GA/jdk11/9/GPL/openjdk-11.0.2_linux-x64_bin.tar.gz
```

Unpack it:

```bash
tar xzfv openjdk-11.0.2_linux-x64_bin.tar.gz
```

define `JAVA_HOME` and add it to `PATH`:

```bash
export JAVA_HOME="${HOME}/spark/jdk-11.0.2"
export PATH="${JAVA_HOME}/bin:${PATH}"
```

check that it works:

```bash
java --version
```

Output:

```
openjdk 11.0.2 2019-01-15
OpenJDK Runtime Environment 18.9 (build 11.0.2+9)
OpenJDK 64-Bit Server VM 18.9 (build 11.0.2+9, mixed mode)
```

Remove the archive:

```bash
rm openjdk-11.0.2_linux-x64_bin.tar.gz
```

### Installing Spark


Download Spark. Use 3.3.2 version:

```bash
wget https://dlcdn.apache.org/spark/spark-3.3.2/spark-3.3.2-bin-hadoop3.tgz

```

Unpack:

```bash
tar xzfv spark-3.3.2-bin-hadoop3.tgz
```

Remove the archive:

```bash
rm spark-3.3.2-bin-hadoop3.tgz
```

Add it to `PATH`:

```bash
export SPARK_HOME="${HOME}/spark/spark-3.3.2-bin-hadoop3"
export PATH="${SPARK_HOME}/bin:${PATH}"
```

### Testing Spark

Execute `spark-shell`:



### PySpark
```bash
export PYTHONPATH="${SPARK_HOME}/python/:$PYTHONPATH"
export PYTHONPATH="${SPARK_HOME}/python/lib/py4j-0.10.9.5-src.zip:$PYTHONPATH"
```

## Note: "lib/py4j-0.10.9.5-src.zip" may be different for you. Check the folder and change it accordingly.