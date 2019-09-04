# dmProcessMonitor
Administrator's tool to monitor Documentum processes (Windows only)

This is a useful but antiquated script I wrote a few years back to monitor the status of Documentum and other related services on Windows servers.  We were experiencing a problem where services would unexpectedly quit.  This tool allowed admins to monitor a select set of services, quickly identify services that had died, and restart them.

The script is written in HTA (Hyper-Text Application), which is essentially VB and run with the mshta.exe script engine.  This technology is deprecated, but still works on Windows 10.

Service names can be obtained from the services.msc control and added to the script.  Many common Documentum and Input Accel service names are already included in the script, you just need to supply the host name/IP.

