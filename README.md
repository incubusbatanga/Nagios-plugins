Unofficial Nagios plugins contributions
=======================================

check_network_device_ping
-------------------------

Logs in to a remote network device, executes device's native 
ping command and parses the results.
  
* Supports several platforms including (but not limited to)
  ios, iosxr and junos and is easily extensible.
  
* Supports pinging inside VRFs and source address/interface
  selection along with other, more common parameters like
  ping timeout, packet count and size.

* Depends only on Net::Telnet Perl module and is otherwise
  self-sufficient.
