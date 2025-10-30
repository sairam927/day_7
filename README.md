# Monitor System Resources Using Netdata
To install **Netdata** using Docker and visualize real-time **system and application performance metrics** such as CPU, memory, disk, and container statistics.
# Tools Used
**Docker** – To run Netdata containerized
**Netdata** – For system monitoring and visualization
**Windows PowerShell** – For executing Docker commands
# commands
[docker --version],
[docker ps].
[docker run -d --name=netdata `
  -p 19999:19999 `
  --cap-add SYS_PTRACE `
  --security-opt apparmor=unconfined `
  -v netdataconfig:/etc/netdata `
  -v netdatalib:/var/lib/netdata `
  -v netdatacache:/var/cache/netdata `
  -v /proc:/host/proc:ro `
  -v /sys:/host/sys:ro `
  netdata/netdata],
[docker ps]
# Access Dashboard
http://localhost:19999
# Monitored Metrics
CPU Usage,
Memory Usage,
Disk I/O,
Network Traffic,
Docker Containers,
System Overview.
# The above are the screenshot of the running Netdata Dashboard
