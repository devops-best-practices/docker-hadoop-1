Hadoop MapReduce demo
=========

Hadoop MapReduce demo with Java


    export HADOOP_CLASSPATH=$JAVA_HOME/lib/tools.jar

    cd hadoop-demo/src/main/java

    hadoop com.sun.tools.javac.Main com/forsrc/hadoop/**/*.java

    jar cf hadoop-demo.jar com/forsrc/hadoop/**/*.class

    hdfs dfs -put com/forsrc/hadoop/wordcount/WordCount.java input/wordcount
    hadoop jar hadoop-demo.jar com/forsrc/hadoop/wordcount/WordCount input/wordcount output/wordcount
    hadoop fs -cat output/wordcount/part-r-00000

    hadoop jar hadoop-demo.jar com/forsrc/hadoop/ncdc/NcdcTemperature input/ncdc output/ncdc
    hadoop fs -cat output/ncdc/part-r-00000

----

```
172.25.0.10       hadoop-master
172.25.0.11       hadoop-slave1
172.25.0.12       hadoop-slave1
```

windows:  ``` route -p add 172.25.0.0 MASK 255.255.255.0 10.0.75.2 ``` or ``` route delete 172.25.0.0 ```