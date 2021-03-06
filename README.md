# AbuseIPDB Scanner

This is a python script that will parse IP addresses from files and interact with AbuseIPDB API. It will return the information about the IP into standard out in tab separated values in standard out.

## Installation

```
git clone https://github.com/mikebanks/AbuseIPdbSCAN.git
```

## Requirements

``` BASH
pip3 install -r requirements.txt
```

## AbuseIPDB API Key

In order to use the script you will need an API key and place it in the script under the "api_key" variable. 
The AbuseIPDB API key information can be found here: (https://www.abuseipdb.com/api.html)

## Usage

Short Form    | Long Form     | Description
------------- | ------------- |-------------
-b            | --block       | lookup an IP block
-c            | --csv         | outputs items in comma seperated values
-d            | --days        | take in the number of days in history to go back for IP reports. Default: 30 Days
-f            | --file        | parses IP Addresses from a single given file
-i            | --ip          | lookup a single IP address
-j            | --json        | outputs items in json format
-l            | --jsonl       | outputs items in jsonl format
-t            | --tsv         | outputs items in tab seperated values (Default)
-x            | --translate   | by default categories are numbers, with this flag it will convert them to text
-v            | --version     | displays version information
-cc           | --countrycode | select a country code to check IP range

### Examples

* To search for reports on an IP address:

``python3 AbuseIPDB.py -i 1.1.1.1``

* To search for reports on an IP Block:

``python3 AbuseIPDB.py -b 1.1.1.0/24``

* To search a whole country IP range and translate the categories to names:

``python3 AbuseIPDB.py -cc nz -x``