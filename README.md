# An Air Quality Sensor Nework Aggregator Using RDFox and Node-RED on Raspberry Pi

The Node-Red code gathers data from a set of air sensors ( see [luftdaten.info](luftdaten.info) for details of sensors) every 5 minutes. The sensors provide PM10 and PM2.5 readings at specified locations (lat, long, alt).  A separate Node-Red flow runs hourly to gather the readings of the previous hour, count the readings per sensor, and calculate min and max.  This data is then sent to RDFox, Allegrograph or any other triplestore that allows SPARQL over HTTP.


Items needed:
* Raspberry Pi 4
* Ubuntu 20.04 
* [RDFox](https://www.oxfordsemantic.tech/product)
* [Node-RED](https://nodered.org/)


Install RDFox and Node-RED on the Pi
Import the 2 flows from the code in the repo
Adjust paths and add credentials for the Allegrograph connection
Start the code by deploying in Node-RED
