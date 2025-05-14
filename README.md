# 🌐 GeoProxy

_Unlock the potential of global web access with GeoProxy_

## Download

```bash
curl -sSf "https://raw.githubusercontent.com/notcoderguy/geoproxy-db/master/HTTP.txt" > HTTP.txt
```

### Format
```bash
######################
#####  HTTP.txt  #####
######################

IP [1]
|
| Port [2]
|   |
|   | Avg. Response Time [3]
|   |   |
|   |   | Google passed [4]
|   |   |  |
|   |   |  |  Anonymity [5]
|   |   |  |   |_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
|   |   |  |_ _ _ _ _ _ _ _ _ _ _ _ _ _ _       | Country [6]
|   |   |_ _ _ _ _ _ _ _                 |      |     |
|   |_ _ _ _ _          |                |      |     |
|             |         |                |      |     |
146.59.70.29:30439,1659.4409942626953,False,Anonymous,FR

1. IP address
2. Port number
3. Avg. Response Time (ms)
4. Google passed
   False = Didn't passed
   True = Passed
5. Anonymity
   Anonymous = Transparent/Anonymous
   Elite = Elite
6. Country

```

### API
[GeoProxy](https://geoproxy.in/) provides a free, robust [API](https://geoproxy.in/api) to narrow down the proxy to your desired specification.

```bash
#######################################################################
#     PARAMETER             VALUES                DESCRIPTION         #
#######################################################################
# FORMAT          | json, txt             | Output format
# ANONYMOUS       | anonymous, elite      | Anonymity level
# TYPE            | http, socks4, socks5  | Proxy protocol
# AMOUNT          | 1-50                  | Proxy results count
# GOOGLE_PASSED   | `Boolean`             | Google passed proxies

#######################################################################
#                           EXAMPLES                                  #
#######################################################################

#######################################################################
# Retrieve one(1) socks5 proxy.                                       #
#######################################################################
curl "https://geoproxy.in/api/socks5?amount=1&format=txt"
> 162.241.46.40:56241

#######################################################################
# Retrieve two(2) http proxies from the US that support https.        #
#######################################################################
curl "https://geoproxy.in/api/http?amount=2&format=txt"
> 80.80.163.190:46276
> 114.132.202.80:8080
```
