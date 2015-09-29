## Geo Lookup Tool

This tool generates latitude, longitude and formatted addresses, given a list of addresses.  
Specifically, it parses a JSON array of objects, searches for the "address", "state" and "zip" fields, and generates "lat", "lng" and "pretty\_address" properties.


### Setup

- you must include your google maps API key, replace the following:
    YOURgoogleAPIcodeGOEShereAFTERtheEQUALsign

- the generator makes use of a "source-file.json" file. a sample has been included

- click "start geolocation" to parse the json file; you will get progress

- you may verify the queries in the console

- once the list has finished parsing, click "create download link", which will export your list to a blob

- click the "download file" link that has been created to access the data. you may then "save as" the blob as a finished json file


### Celtra Notes

Celtra's map engine will search for the "address" property and ignore "pretty\_address". After you convert the JSON file to a CSV/XLS for use with Celtra, it is important to:

- delete the "address" column
- rename "pretty\_address" to "address"
- make sure that the "lat" and "lng" columns appear *before* (to the left of) the "address" column

This way, Celtra will find lat + lng first and will not attempt to geo-locate by itself, which usually yields poor results.






