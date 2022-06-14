# Docker-compose-file-snort

## Requirements
You need to install `Docker` and `Dockercompose`



## Rules write /etc/snort/rules/local.rules

`alert icmp any any -> any any (msg:"ICMP Echo Request"; itype:8; sid:10000;)`
`alert icmp any any -> any any (msg:"ICMP Echo Reply"; itype:0; sid:10001;)`

## Bash Command
`docker-compose up -d`

`docker-compose exec snort idstools-u2json @/etc/snort/u2json.conf`


`tail -f data/log/alert.json`
