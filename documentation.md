## Window Sensor documentation



### SIOT Connection string and json definition for APP Team
```
labenv
NexHome$1
https://siot.net:19025

mqtt://siot.net 1883

siot/DAT/60CE-EF63-AE15-78F7-6F84-45B9-FD75-037F/9a24aae2-0dda-2feb-1414-cf9dbbc2e404

{
	"windowId": "windowID"
	"Open": "true/false"
}
```


### Open ZWave Shared Nodejs script to connect
[Open ZWave Shared](https://github.com/OpenZWave/node-openzwave-shared/blob/master/README-raspbian.md)

```
node12: changed: 113:Alarm Type:0->0
node12: changed: 113:Alarm Level:0->0
node12: changed: 113:SourceNodeId:0->0
node12: changed: 113:Access Control:23->22
```

### ZWave2MQTT Bridge
Simple Brigde with Web based interface to configure the zwave and mqtt connection.


https://github.com/OpenZWave/Zwave2Mqtt

```
git clone https://github.com/OpenZWave/Zwave2Mqtt
cd Zwave2Mqtt
npm install
npm run build
npm start
```

### Reconnect after restart of node (Wake up strip)
* How to manually wake up Strips Guard
* Move magnet over the user command sensor 3 times ( 3 LED blinks)
* 5 short blinks indicates failure. Try again or contact customer support 

### Meaning of values
22 = open
23 = closed

### Todo
Node Red flow zwave to mqtt.

22 = true
23 = closed

And set window ID