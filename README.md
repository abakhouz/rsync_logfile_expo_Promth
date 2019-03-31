
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
##  Test input file /var/log/rsync.log

##  http://34.241.68.83:8000

# HELP rsync_all_transferred_bytes_total Show all transferred bytes
# TYPE rsync_all_transferred_bytes_total counter
rsync_all_transferred_bytes_total 1.813295136e+09
# TYPE rsync_all_transferred_bytes_created gauge
rsync_all_transferred_bytes_created 1.554055909667079e+09
# HELP rsync_unique_connections_total Count all unique peers
# TYPE rsync_unique_connections_total counter
rsync_unique_connections_total 6.0
# TYPE rsync_unique_connections_created gauge
rsync_unique_connections_created 1.554055909667065e+09
# HELP rsync_all_connections_total Count all opened connections
# TYPE rsync_all_connections_total counter
rsync_all_connections_total 6.0
# TYPE rsync_all_connections_created gauge
rsync_all_connections_created 1.554055909667044e+09
# HELP python_info Python platform information
# TYPE python_info gauge
python_info{implementation="CPython",major="2",minor="7",patchlevel="5",version="2.7.5"} 1.0
# HELP process_virtual_memory_bytes Virtual memory size in bytes.
# TYPE process_virtual_memory_bytes gauge
process_virtual_memory_bytes 4.47377408e+08
# HELP process_resident_memory_bytes Resident memory size in bytes.
# TYPE process_resident_memory_bytes gauge
process_resident_memory_bytes 1.3185024e+07
# HELP process_start_time_seconds Start time of the process since unix epoch in seconds.
# TYPE process_start_time_seconds gauge
process_start_time_seconds 1.55405590879e+09
# HELP process_cpu_seconds_total Total user and system CPU time spent in seconds.
# TYPE process_cpu_seconds_total counter
process_cpu_seconds_total 10.98
# HELP process_open_fds Number of open file descriptors.
# TYPE process_open_fds gauge
process_open_fds 10.0
# HELP process_max_fds Maximum number of open file descriptors.
# TYPE process_max_fds gauge
process_max_fds 4096.0

===========================================


A quick guide on how to instrument an application can be found here:

- https://prometheus.io/docs/instrumenting/clientlibs/
- https://prometheus.io/docs/instrumenting/writing_exporters/


