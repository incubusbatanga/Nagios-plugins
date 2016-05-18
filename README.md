Miscellaneous Nagios plugins
============================

check_network_device_ping
-------------------------

Logs onto a remote network device, executes device's native
ping command and parses the results. To avoid establishing
hundreds of telnet sessions to the same device and to circumvent
CLI session limits imposed by some platforms (ie. Cisco IOS's
5 vtys), pinging is done by a background process ('daemon')
started once per network device. Each daemon will keep a CLI
session open as long as there are checks to be performed.
If left idle, daemons will die out after a (configurable)
period of inactivity. This way, all checks performed by one
device are controlled by a single remote CLI session, as long
as those checks are not too far apart.

Features:

* Supports several platforms including (but not limited to)
  ios, iosxr and junos and is easily extensible.

* Supports pinging inside VRFs and source address/interface
  selection along with other, more common parameters like
  ping timeout, packet count and size.

* Basically depends only on Net::Telnet module, as other
  required modules are either already included in Perl
  distribution or installed on most systems by default.
