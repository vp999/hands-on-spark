# Installation

1. Visit:  http://spark.apache.org/downloads.html

2. Select following options

  1. Choose a Spark release: *2.2.x* or greater (I'll be using 2.2.1)
  2. Choose a package type:  *Pre-built for Apache Hadoop 2.7 and later*
  3. Download Spark: *spark-2.2.1-bin-hadoop2.7.tgz*

    Download that tar compressed file to your local machine.

3. After downloading the compressed file, unzip it to desired location:

    `$ tar -xvzf spark-2.2.1-bin-hadoop2.7.tgz -C ~/tools/spark-2.2.1/`

4. Setting up the environment for Spark:

  To set up environment variable: <br>
  Add following lines to your `~/.bashrc`

```
  export SPARK_HOME=/Users/nipunsadvilkar/tools/spark-2.2.1-bin-hadoop2.7
  export PATH=$SPARK_HOME/bin:$PATH
```


   Make sure you change the path in `SPARK_HOME` as per your spark software file are located.
   Reload your `~/.bashrc` file using:

  ```
  $ source ~/.bashrc
  ```

5. That's all! Spark has been set-up. Try running `pyspark` command to use Spark from Python.
