Role for installing components, tools and libraries on EC2

## Requirements

EMR or Hadoop cluster

## Role variables

Available variables are listed below, along with the default values (see `defaults/main.yml)

```
hadoop_tools_hadoop_version: 2.8.5
hadoop_tools_hadoop_tarball_url: "http://apache.newfountain.nl/hadoop/common/hadoop-{{ hadoop_tools_hadoop_version }}/hadoop-{{ hadoop_tools_hadoop_version }}.tar.gz"

hadoop_tools_hive_version: 2.3.6
hadoop_tools_hive_tarball_url:  "http://apache.40b.nl/hive/hive-{{ hadoop_tools_hive_version }}/apache-hive-{{ hadoop_tools_hive_version }}-bin.tar.gz"

hadoop_tools_spark_version: 2.4.4
hadoop_tools_spark_tarball_url: "https://archive.apache.org/dist/spark/spark-{{ hadoop_tools_spark_version }}/spark-{{ hadoop_tools_spark_version }}-bin-without-hadoop.tgz"

hadoop_tools_oozie_version: 5.1.0
hadoop_tools_oozie_tarball_url: "http://apache.40b.nl/oozie/{{ hadoop_tools_oozie_version }}/oozie-{{ hadoop_tools_oozie_version }}.tar.gz"

hadoop_tools_maven_tarball_url: "http://us.mirrors.quenda.co/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz"
```

## Dependenices

Java role

## Sample playbook

```
---

- hosts: target_host
  become: yes
  become_user: root
  roles:
    - hadoop-tools
```


