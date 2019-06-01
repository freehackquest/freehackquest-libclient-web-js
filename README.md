# libfhqcli-web-js

JavaScript Client Library for fhq-server: [https://github.com/freehackquest/fhq-server.git](https://github.com/freehackquest/fhq-server.git)


## Install
```
npm install --save libfhqcli-web-js
```
## Example code

Include script ```dist/libfhqcli-web-js.js```

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

After success connection you can call [API.md](https://github.com/freehackquest/libfhqcli-web-js/blob/master/API.md)
