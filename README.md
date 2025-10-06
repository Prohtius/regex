## Get only the space between vlan number and 802.1q 
e.g. _vlan 994 802.1q 1/1_
```regex
    (?<=\d)(?<=\d)(?<=\d)\s(?=802)
    
    (?<=\d)(?<=\d)(?<=\d)\s".*"
```
## Select "TAG..." in string
e.g. _vlan 999 802.1q 1/1 "TAG PORT 3/50 VLAN 127"_
```regex
    (?<=\/\d{1,2})\s".*"
``` 
## Select from the end of the subnet mask to the end of the line
e.g. _ip interface "HS-Wired" address 10.1.254.1 mask 255.255.255.0 vlan 10 ifindex 1_
```regex
    (?!\d{1,})\svlan\s\d{1,}.*
```
## Select only "lichgames" from URL 
```regex
    (?!https://)lichgames(?=.s3.amazonaws.com)
```
## exlude tv.apple.com from exceptions ^([A-Za-z0-9.-]*\.)?apple\.com\.? (case insensitive)
```regex
    ^(?!tv)([A-Za-z0-9.-]*\.)?apple\.com\.?/gmi
```
## exlude tv.apple.com from exceptions ^([A-Za-z0-9.-]*\.)?apple\.com\.? (case sensitive)
```regex
    ^(?!tv)(?!TV)([A-Za-z0-9.-]*\.)?apple\.com\.?#
```
