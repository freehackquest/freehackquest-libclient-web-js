# freehackquest-libclient-web-js

[![Total alerts](https://img.shields.io/lgtm/alerts/g/freehackquest/freehackquest-libclient-web-js.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/freehackquest/freehackquest-libclient-web-js/alerts/) [![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/freehackquest/freehackquest-libclient-web-js.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/freehackquest/freehackquest-libclient-web-js/context:javascript) [![npm](https://img.shields.io/npm/v/freehackquest-libclient-web-js)](https://www.npmjs.com/package/freehackquest-libclient-web-js)

JavaScript Client Library for fhq-server: [https://github.com/freehackquest/fhq-server.git](https://github.com/freehackquest/fhq-server.git)


## Install
```
npm install --save freehackquest-libclient-web-js
```
## Example code

Include script ```dist/freehackquest-libclient-web-js.js```

```
fhq.bind('notify', function(data){
    console.log('notify: ' + JSON.stringify(data))
});

fhq.bind('connected', function(data) {
    console.log('connected: ' + JSON.stringify(data))
});

fhq.bind('disconnected', function(data) {
    console.log('disconnected: ' + JSON.stringify(data))
});

fhq.bind('userdata', function(data) {
    console.log('userdata: ' + JSON.stringify(data))
});

// connect
fhq.init({
    'baseUrl': ws://' + window.location.hostname + ':1234/api-ws/
});

// for disconnect call fhq.deinit()
```

After success connection you can call [API.md](https://github.com/freehackquest/freehackquest-libclient-web-js/blob/master/API.md)
