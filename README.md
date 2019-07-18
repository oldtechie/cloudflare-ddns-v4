# cloudflare-ddns-v4
v4 scripts to manage ddns records

This is the working script gleaned from cloudflare ages ago.

It's version 4 of the script, which has been homed on an ubuntu 14 server for long time, working as of July 2019...
Now here as part of moving to a docker.
All it needs to know is the usual, plus the record it's interested in.
It goes & gets the ID with an API call, using cURL and updating only if necessary due to change since last check.
Force re-write by changing the contents of the ip.txt file.
Needs to be put into CRON to run every hour, or however frequently you consider necessary.
;-)
Adjustment:

Currently the process is:

 check current real-world IP (ipconfig.co / icanhazip.com etc) and compare to ip.txt
 
 dig @1.1.1.1 +short dragon.hiscott.net > ip2.txt
 
 if different - then go through update process so record XXX is set to current real-world-ip

Needs to change so that an nslookup check on current record XXX value is done (and put into ip.txt?)

Then compare real-world-IP with XXX record

Then go through change process if required
