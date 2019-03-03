# curl Cheetsheet

## HTTP methods
```
curl --request <METHOD> <url>
```

|  No |  Method | curl  |
|---|---|---|
| 1 | GET | curl --request GET https://url/object/id |
| 2 | POST | curl --request POST https://url/ |
| 3 | DELETE | curl --request DELETE https://url/object/id/ |
| 4 | PUT | curl --request PUT https://url/object/id/ |

## HTTP request with data
*Use -d or --data to attach data with curl request*
```
curl -X POST <url> -d 'property1=value1,property2=value2'

curl -X POST https://url/login/ -d 'username=yourusername&password=yourpassword'
```

## Return only the HTTP Headers of a URL
*Use -I to view HTTP headers*
```
curl -I <url>

curl -I https://url
```

## Save result of a curl command with pre-defined filename
```
curl -o <url>

curl -o https://url
```

## Save result of a curl command with custom filename
```
curl <url> --output <file-name>

curl https://url/object/id/ --output test.txt
```

## Add additional HTTP headers
*Headers must be followed by a semi-colon*
```
curl -H 'X-Header: Value' <url>

curl -H 'Custome-Header: custom-header' https://url
```

## Resume download
```
curl -C -O <url>

curl -C -O https://url/object/id/
```
