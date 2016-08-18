# OAuth2AuthServer
OAth2 Authentication Server. Need this to run the first app with OAuth properties.

1) Run the "MyFirstApplication" 

2) Run this application

3) Run curl http://localhost:8080/resource/test 

Will not be able to access

4) Run 

curl -XPOST -k foo:foosecret@localhost:9000/hascode/oauth/token \
   -d grant_type=password -d client_id=foo -d client_secret=abc123 \
   -d username=bar -d password=barsecret 
   
Get the Token and other details.

5) Copy paste the token into "TOKEN" variable

6) curl -H "Authorization: Bearer $TOKEN" http://localhost:8080/resource/test

Will see the "Hello" message.


Can run other URLS using post commands or GET commands

Sample URLs:

http://localhost:8080/device/partofmap/16/23
http://localhost:8080/device/findFromDate/2020-09-04T05:08:56.235-0400
http://localhost:8080/device/findById/57b4fd6a9223d17342873882
http://localhost:8080/device/listwithname/Device4
etcc..


POST case: Through Desktop postman: To Save :
URL : http://localhost:8080/device/
In Request Header, Set Key "Content-Type" to value "application/json".
In Request Body, send something like below:
{
"deviceName" : "Device18",
"eventType" : "Automated type",
"eventDate" : "2010-09-04T05:08:56.235-0400",
"eventCount" : "30"
}

Response would be something like : 
{
  "deviceId": "57b5bbd49223d1739b7c8bc0",
  "deviceName": "Device18",
  "eventType": "Automated type",
  "eventCount": 30,
  "eventDate": 1283591336235
}
 
   
