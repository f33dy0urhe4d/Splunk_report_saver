##### REPORTSAVER

You can find log files here:
	cat /opt/splunk/splunk/var/log/splunk/python.log | grep REPORTSAVER
	cat /opt/splunk/splunk/var/log/splunk/pdfgen.log | grep REPORTSAVER

Files Involved:
	/opt/splunk/splunk/etc/apps/u_lgm_infrastructure/lookups/reportsaver.csv -> CSV containing reports that has to be handled by REPORTSAVER
	/opt/splunk/splunk/etc/system/bin/pdfgen_endpoint.py -> Splunk customized pdfgen endpoint handling pdfsave on filesystem


########## REPORTSAVER INSTALLATION PROCEDURE

cp /opt/splunk/splunk/etc/system/bin/pdfgen_endpoint.py /opt/splunk/splunk-backup/pdfgen_endpoint.py.orig
cp reportsaver/pdfgen_endpoint.py /opt/splunk/splunk/etc/system/bin/pdfgen_endpoint.py

chown ussplunk:splunk /opt/splunk/splunk/etc/system/bin/pdfgen_endpoint.py
