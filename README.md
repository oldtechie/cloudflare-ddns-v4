# cloudflare-ddns-v4
v4 scripts to manage ddns records

This is the working script gleaned from cloudflare ages ago.

It's version 4 of the script, which has been homed on an ubuntu 14 server for long time, now here as part of moving to a docker.
All it needs to know is the usual, plus the record it's interested in.
It goes & gets the ID with an API call, using cURL and updating only if necessary due to change since last check.
Force re-write by changing the contents of the ip.txt file.
Needs to be put into CRON to run every hour, or however frequently you consider necessary.
;-)
