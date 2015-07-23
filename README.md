# NET HEALER 
###Centralizes DDoS Attack Reports from multiple collectors<br>Analyze, classify, notify and mitigate

NET HEALER supports FastNetMon and Plixer Scrutinizer DDoS attack reports.<br>
It groups them for further algorithms run on taking decisions. 
<br>i.e: trigger notification or BAN an IP based on pre-configured protocol thresholds.

It works on four different stages 
- cleared - none Attack Reports received.
- warning - A few Attack Report(s) received
- critical - Notify and run attack classification algorithms for further inspection
- under_attack - Notify and enable DDoS mitigation

It will support actions / stage:
 - email
 - flowdock / slack / pagerduty notifications
 - execute a script

## Requirement
- Redis database
- FastNetMon: a super cool tool written by Pavel Odintsov - https://github.com/FastVPSEestiOu/fastnetmon
- Plixer Scrutinizer (optional)

##Starting up

1. `script/bootstrap`
2. Populate `.env` with a config
3. `script/start`

<br>
##Available functions

### query
GET /healer/v1/ddos/status => query DDoS status

GET /healer/v1/ddos/reports => query DDoS alarms details

GET /healer/v1/ddos/brief => query DDoS alarms brief

### WORK IN PROGRESS. <br>PRs are more than welcome !
