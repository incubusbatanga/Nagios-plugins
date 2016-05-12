Unofficial Nagios plugins contributions
=======================================

check_network_device_ping
-------------------------

Logs in to a remote network device, executes device's native
ping command and parses the results. To circumvent CLI session
limits imposed by some platforms (ie. Cisco IOS's 5 vtys) and
to generally reduce the number of open connections, the actual
pinging is done by a background process ('daemon') started
once per network device. It will keep the CLI session open
as long as there are checks to be performed from the same
device and die out after a (configurable) period of inactivity.
This way, all checks from one device are done over a single
remote CLI session as long as those checks are not too far
apart.

Features:

* Supports several platforms including (but not limited to)
  ios, iosxr and junos and is easily extensible.

* Supports pinging inside VRFs and source address/interface
  selection along with other, more common parameters like
  ping timeout, packet count and size.

* Basically depends only on Net::Telnet module and is otherwise
  self-sufficient. That is, other modules it requires are either
  already included in your Perl distribution or installed by
  default on your system.
