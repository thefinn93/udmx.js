# uDMX.js

A library to interact with uDMX dongles

Sample usage:

```javascript
#!/usr/bin/env nodejs

var uDMX = require('udmx');

var dmx = new uDMX();

dmx.on('channel-all', (channel, value) => {console.log(channel + ' => ' + value);});
dmx.on('connected', () => {console.log('Connected');});

dmx.connect();

setInterval(() => {dmx.set(Math.round(Math.random() * 512), Math.round(Math.random() * 255));}, 1000);
```

