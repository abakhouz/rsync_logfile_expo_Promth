
## Files
prometheus.py	# Main file. You should start this file
argchecker.py	# This file contains the argument checks. 
metrics.py	# This file store the method what used to fill the metrics

## Metrics
all_conn	# Count all started connections since agent start 
all_conn_unique_cource # Count all unique connections
all_bytes_transferred # Count all bytes whattransferred since agent started

## Application
Exporter port: 8000 Referring to [Prometheus_Ports](https://prometheus.io/docs/instrumenting/writing_exporters/)

Start the application with the following command
```
$ ./prometheus_exporter /var/log/rsync.log
```
##  Test input file 
rsync.log

##  http://34.241.68.83:8000
result_test_rsync_log  

===========================================


A quick guide on how to instrument an application can be found here:

- https://prometheus.io/docs/instrumenting/clientlibs/
- https://prometheus.io/docs/instrumenting/writing_exporters/


