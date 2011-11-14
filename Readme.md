Socket.IO RedisStore
===

### Use it:

(requires socket.io >= 0.8.5):

```javascript
var sio = require('socket.io')
  , RedisStore = sio.RedisStore
  , io = sio.listen()

io.configure(function () {
  io.set('store', new RedisStore)
})
```

### Persist it:

```javascript
io.sockets.on('connection', function(socket) {
  var nick = 'dshaw'
  socket.set('nickname', nick, function() {
    socket.emit('nickname', nick)
  })
})
```

### Scale it:

Point all socket.io processes and server instances at the same Redis server.

```javascript
io.configure(function () {
  io.set('store', new RedisStore({ host: 'http://redis.example.com' }))
})
```

### Resources:
  - [redis.io](https://redis.io)
  - [socket.io](http://socket.io/)
  - [socket.io mailing list](http://groups.google.com/group/socket_io)
  - [#socket.io on freenode.net](http://webchat.freenode.net?channels=socket.io&uio=d4)
