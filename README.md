# Installation

1. Visit Apache Spark Downloads page

    http://spark.apache.org/downloads.html

2. Select following options
    1. Choose a Spark release: **2.2.x** or greater (I'll be using 2.2.1)
    2. Choose a package type:  **Pre-built for Apache Hadoop 2.7 and later**
    3. Download Spark: **spark-2.2.1-bin-hadoop2.7.tgz**

    Download that tar compressed file to your local machine.

3. After downloading the compressed file, unzip it to desired location:

    `$ tar -xvzf spark-2.2.1-bin-hadoop2.7.tgz -C ~/tools/spark-2.2.1/`

4. Setting up the environment for Spark:

    To set up environment variable:
    
    Add following lines to your `~/.bashrc`

    ```bash
    export SPARK_HOME=/Users/nipunsadvilkar/tools/spark-2.2.1-bin-hadoop2.7
    export PATH=$SPARK_HOME/bin:$PATH
    ```
    Make sure you change the path in `SPARK_HOME` as per your spark software file are located.
    Reload your `~/.bashrc` file using:

    ```
    $ source ~/.bashrc
    ```

5. That's all! Spark has been set-up. Try running `pyspark` command to use Spark from Python.


## Pyspark in Jupyter Notebook

Two methods to do so.

1. Configure PySpark driver
    Update PySpark driver environment variables: add these lines to your ~/.bashrc (or ~/.zshrc) file.

    ```bash
    export PYSPARK_DRIVER_PYTHON=jupyter
    export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
    ```
    
    Restart your terminal and launch PySpark again:

    `$ pyspark`

    Now, this command should start a Jupyter Notebook in your web browser.

2. Using `findspark` module
    
    findSpark package is not specific to Jupyter Notebook, you can use this trick in your favorite IDE too.

    To install findspark:

    `$ pip install findspark`

    Irrespective of Jupyter notebook/Python script all you need to do to use spark is add following line in your code:

    ```python
    import findspark
    findspark.init()
    ```