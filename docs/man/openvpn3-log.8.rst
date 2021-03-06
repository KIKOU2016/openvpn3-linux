============
openvpn3-log
============

----------------------
OpenVPN 3 Linux client
----------------------

:Manual section: 8
:Manual group: OpenVPN 3 Linux

SYNOPSIS
========
| ``openvpn3 log`` ``[OPTIONS]``
| ``openvpn3 log`` ``-h`` | ``--help``


DESCRIPTION
===========
This retrieves log events from various log senders and prints it to the
terminal.  The user running this command must in advanced have been granted
access to these log events, otherwise it will not generate any output.

Log events received via ``openvpn3 log`` are processed in parallel with the
system wide ``openvpn3-service-logger`` process.


OPTIONS
=======

-h, --help      Print  usage and help details to the terminal

--session-path SESSION-DBUS-PATH
                D-Bus session path to a running VPN session to retrieve log
                events from.  Use ``openvpn3 sessions-list`` to retrieve a list
                of available session D-Bus paths.

--log-level LEVEL
                Sets the log verbosity for the log events.  Valid values are
                *0* to *6*.  The higher value, the more verbose the log events
                will be.  Log level *6* will retrieve all debug events.

--config-events
                Retrieve log events from the configuration manager.  For this
                to work, the ``openvpn3-service-configmgr`` must have been
                started with ``--signal-broadcast``.


SEE ALSO
========

``openvpn3``\(8)
``openvpn3-service-configmgr``\(8)
``openvpn3-service-logger``\(8)
``openvpn3-session-acl``\(8)