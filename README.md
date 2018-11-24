Invoke-AkamaiOPEN
========================================

EdgeGrid Powershell

NOTICE : PowerShell EdgeGrid Client has been deprecated and will reach End of Life soon. For more information, please see our [Announcement](https://developer.akamai.com/blog/2018/11/13/akamai-powershell-edgegrid-client-end-life-notice)

## SUMMARY

Invoke-AkamaiOPEN is a Powershell 'authorization' wrapper around Invoke-RestMethod. It adds the required EdgeGrid signature to a normal Invoke-RestMethod request.

Invoke-AkamaiOPEN requires Powershell 3.0

## CONFIGURATION

The parameters and credentials for signing the requests are passed during runtime as command line options

## OPERATION

Available command line options are:
* `-Method` Request method. Valid values are GET, POST, PUT, and DELETE
* `-ClientToken` Authentication token used in client auth. Available in Luna Portal.
* `-ClientAccessToken` Authentication token used in client auth. Available in Luna Portal.
* `-ClientSecret` Authentication password used in client auth. Available in Luna Portal.
* `-ReqURL` Full request URL complete with API location and parameters. Must be URL encoded.
* `-Body` Should contain the POST/PUT Body. The body should be structured like a JSON object. Example: $Body = '{ "name": "botlist2", "type": "IP", "list": ["201.22.44.12", "8.7.6.0/24"] }'

## EXAMPLE

```
Invoke-AkamaiOPEN -Method GET -ClientToken "foo" -ClientAccessToken "foo" -ClientSecret "foo" -ReqURL "https://foo.luna.akamaiapis.net/diagnostic-tools/v1/locations"
```
