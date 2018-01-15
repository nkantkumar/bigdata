(1) To check direcry exist in the HDFS or not

if $(hdfs dfs -test -d /nishi) ; then echo "ok";else echo "not ok"; fi

(2) no such method error org.apache.parquet.column.ParquetProperties.builder()Lorg/apache/parquet/column/ParquetProperties$Builder;

<dependency>
			<groupId>org.apache.parquet</groupId>
			<artifactId>parquet-generator</artifactId>
			<version>1.9.0</version>
		</dependency>
		<dependency>
			<groupId>org.apache.parquet</groupId>
			<artifactId>parquet-hadoop</artifactId>
			<version>1.9.0</version>
		</dependency>
		<dependency>
			<groupId>org.apache.parquet</groupId>
			<artifactId>parquet-common</artifactId>
			<version>1.9.0</version>
		</dependency>
		<dependency>
			<groupId>org.apache.parquet</groupId>
			<artifactId>parquet-column</artifactId>
			<version>1.9.0</version>
		</dependency>
(3) com.google.protobuf.InvalidProtocolBufferException: Protocol message end-group tag did not match expected tag.; Host Details : local host is: "nishikants-MacBook-Pro.local/192.168.1.68"; destination host is: "192.168.1.68":50070; 

provide the namenode url: check core-site.xml and fs.default.name
hdfs://localhost:9000/

(4) java.lang.NoSuchMethodError: org.apache.commons.lang3.time.FastDateFormat.parse(Ljava/lang/String;)Ljava/util/Date

<dependency>
			<groupId>org.apache.commons</groupId>
			<artifactId>commons-lang3</artifactId>
			<version>3.7</version>
		</dependency>

(5) 
Caused by: java.lang.IllegalArgumentException: Error while instantiating 'org.apache.spark.sql.hive.HiveExternalCatalog':
	at org.apache.spark.sql.internal.SharedState$.org$apache$spark$sql$internal$SharedState$$reflect(SharedState.scala:169)
	at org.apache.spark.sql.internal.SharedState.<init>(SharedState.scala:86)

sol- chmod 777 /tmp/hive			