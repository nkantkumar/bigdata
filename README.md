(1) To check direcry exist in the HDFS or not
if $(hdfs dfs -test -d /nishi) ; then echo "ok";else echo "not ok"; fi