**Question 1:**



**问题描述：**spark-shell初始化SparkContext失败



**报错信息：**

WARN SparkContext: Multiple running SparkContexts detected in the same JVM! 	

org.apache.spark.SparkException: Only one SparkContext may be running in this JVM



**问题解决**：**Spark-shell already prepares a spark-session or spark-context**

去掉 

val sparkConf = new SparkConf().setAppName("wordCount")

val sc = new SparkContext(sparkConf)

