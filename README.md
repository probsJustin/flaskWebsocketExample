# Test application for websockets 

First tutorial and example found here: 
https://blog.miguelgrinberg.com/post/easy-websockets-with-flask-and-gevent

Wanted to create some examples to use in future projects and do some simple testing with a couple of theories about a previous hackathon project

### Working Clone-able Example: 

https://github.com/miguelgrinberg/Flask-SocketIO

### Websocket examples 

```buildoutcfg
$(document).ready(function(){
    var socket = io.connect('http://' + document.domain + ':' + location.port + '/test');
    socket.on('my response', function(msg) {
        $('#log').append('<p>Received: ' + msg.data + '</p>');
    });
    $('form#emit').submit(function(event) {
        socket.emit('my event', {data: $('#emit_data').val()});
        return false;
    });
    $('form#broadcast').submit(function(event) {
        socket.emit('my broadcast event', {data: $('#broadcast_data').val()});
        return false;
    });
});
```


### End result: 
Implementing something like this to an API end point/method to do some basic examples with MQ and some other infra testing to log "in real time"
https://stackoverflow.com/questions/29266594/broadcast-to-all-connected-clients-except-sender-with-python-flask-socketio