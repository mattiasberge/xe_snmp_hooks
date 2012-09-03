xenserver_snmp
==============

You can read more here: http://nohup.mooo.com/monitoring-xenserver-over-snmp-using-opennms/


snmpd config that uses the XenServer tools (xe) to get hypervisor performance metrics. 

$ grep cpu28 snmpd.conf

exec .1.3.6.1.4.1.2021.99.10.99.10.31.0.28 "cpu28" /opt/xensource/bin/xe host-data-source-query data-source=cpu28


$ snmpwalk -c public -v 2c 10.99.10.31 .1.3.6.1.4.1.2021.99.10.99.10.31.0.28

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.1.1 = INTEGER: 1

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.2.1 = STRING: "cpu28"

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.3.1 = STRING: "/opt/xensource/bin/xe host-data-source-query data-source=cpu28"

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.100.1 = INTEGER: 0

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.101.1 = STRING: "0.014319"

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.102.1 = INTEGER: 0

iso.3.6.1.4.1.2021.99.10.99.10.31.0.28.103.1 = ""
