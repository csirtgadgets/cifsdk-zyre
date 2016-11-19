# Getting Started
The CIF-Zyre framework reads in [csirtg-indicator](https://github.com/csirtgadgets/csirtg-indicator-py) messages from a [ZYRE](http://rfc.zeromq.org/spec:36/ZRE) mesh network and POSTs them to a local [CIFv3](https://github.com/csirtgadgets/bearded-avenger) instance via the [cifsdk](https://github.com/csirtgadgets/bearded-avenger-sdk-py).

```bash
$ pip install cifsdk_zyre
$ cif-zyre -h
$ cif-zyre --remote https://localhost --token 1234 -i tap0 -d
```

# Examples
```
2016-11-19 14:52:37,196 - INFO - cifsdk_zyre.client[134][MainThread] - [SHOUT:Willie Gonzales] {
    "additional_data": null,
    "application": null,
    "asn": null,
    "asn_desc": null,
    "cc": null,
    "city": null,
    "confidence": null,
    "description": null,
    "firsttime": "2016-11-19T14:52:44.331459Z",
    "group": null,
    "indicator": "192.168.1.2",
    "itype": "ipv4",
    "lasttime": "2016-11-19T14:52:44.331459Z",
    "latitude": null,
    "longitude": null,
    "peers": null,
    "portlist": 22,
    "protocol": "tcp",
    "provider": null,
    "rdata": null,
    "reference": null,
    "reference_tlp": null,
    "reporttime": null,
    "tags": [
        "scanner",
        "ssh"
    ],
    "tlp": null,
    "version": "0.00a0"
}
2016-11-19 14:52:37,199 - DEBUG - cifsdk.client.http[168][MainThread] - https://localhost/indicators
2016-11-19 14:52:37,205 - DEBUG - requests.packages.urllib3.connectionpool[809][MainThread] - Starting new HTTPS connection (1): 172.31.12.183
2016-11-19 14:52:37,597 - DEBUG - requests.packages.urllib3.connectionpool[400][MainThread] - https://localhost:443 "POST /indicators HTTP/1.1" 201 40
2016-11-19 14:52:37,598 - DEBUG - cifsdk.client.http[104][MainThread] - {
  "data": 1, 
  "message": "success"
}
```

# Getting Involved
There are many ways to get involved with the project. If you have a new and exciting feature, or even a simple bugfix, simply [fork the repo](https://help.github.com/articles/fork-a-repo), create some simple test cases, [generate a pull-request](https://help.github.com/articles/using-pull-requests) and give yourself credit!

If you've never worked on a GitHub project, [this is a good piece](https://guides.github.com/activities/contributing-to-open-source) for getting started.

# Development
## Some of the tools we use:

* [PyCharm](https://www.jetbrains.com/pycharm/)
* [VirtualenvWrapper](https://virtualenvwrapper.readthedocs.org/en/latest/)
* [Vagrant](https://www.vagrantup.com/)

# COPYRIGHT AND LICENCE

Copyright (C) 2016 [the CSIRT Gadgets Foundation](http://csirtgadgets.org)

Free use of this software is granted under the terms of the GNU Lesser General Public License (LGPLv3). For details see the files `COPYING` included with the distribution.
