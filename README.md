# dmProcessMonitor
Administrator's tool to monitor Documentum processes (Windows only)

This is a useful (but antiquated) script I wrote a few years back to monitor the status of Documentum and other related services on Windows servers.  We were experiencing a problem where services would unexpectedly quit.  This tool allowed admins to monitor a select set of services, quickly identify services that had died, and restart them.

The script is written in HTA (Hyper-Text Application), which is essentially VB and run with the mshta.exe script engine.  This technology is deprecated, but still works on Windows 10.

Service names can be obtained from the services.msc control and added to the script.  Many common Documentum and Input Accel service names are already included in the script, you just need to supply the host name/IP.  For example:

<pre>
	arrProcessList.add("192.168.0.101:DmDocbroker")
	arrProcessList.add("192.168.0.101:DmServerrepo1")
	arrProcessList.add("192.168.0.101:Tomcat7")
	arrProcessList.add("192.168.0.101:MSSQLSERVER")
	arrProcessList.add("192.168.0.101:DmMethodServer")
	arrProcessList.add("192.168.0.101:DmPrimaryDsearch")
  </pre>

The script can be configured to refresh itself periodically by setting a value greater than 30 in the Refresh Internval field.  Or, a refresh can be conducted on demand by clicking the Refresh Now button.  Services can be stopped and started by using the button associated with its name i nthe display.

Of course, the entire script can be modified to your needs.

![](https://github.com/msroth/dmProcessMonitor/blob/master/Capture.PNG)
