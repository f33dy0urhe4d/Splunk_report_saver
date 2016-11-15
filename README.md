# README #

Custom implementation of pdfgen_endpoint.py that allows saving scheduled-PDF dashboards locally.

### What is this repository for? ###

* Allowing to save scheduled-PDF dashboards locally
* Version: 6.3.4

### How do I get set up? ###

* cp /opt/soc/splunk/etc/system/bin/pdfgen_endpoint.py /opt/soc/splunk-backup/pdfgen_endpoint.py.orig
* cp reportsaver/pdfgen_endpoint.py /opt/soc/splunk/etc/system/bin/pdfgen_endpoint.py
* chown ussplunk:$(id -g ussplunk) /opt/splunk/splunk/etc/system/bin/pdfgen_endpoint.py

### Involved Files ###

* /opt/soc/splunk/etc/apps/u_lgm_infrastructure/lookups/reportsaver.csv: CSV containing reports that has to be handled by REPORTSAVER
* /opt/soc/splunk/etc/system/bin/pdfgen_endpoint.py -> Splunk customized pdfgen endpoint handling pdfsave on filesystem

### Log Files ###

* cat /opt/soc/splunk/var/log/splunk/python.log | grep REPORTSAVER
* cat /opt/soc/splunk/var/log/splunk/pdfgen.log | grep REPORTSAVER

### Who do I talk to? ###

* Moviri SpA