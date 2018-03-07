FROM scylladb/scylla

RUN sed -i "s/#SCYLLA_JMX_REMOTE=\"-r\"/SCYLLA_JMX_REMOTE=\"-r\"/g"  /etc/sysconfig/scylla-jmx
ADD scyllasetup.py /
ADD scylla-jmx-service.sh /
