#RedisStore Configuration


##RedisStore([options])

```javascript
io.configure(function () {
  io.set('store', new RedisStore({ host: 'http://redis.example.com' }))
})
```

##options parameters

`options.nodeId` (fn): id generator function. default will generate a random unique id.

`options.redis` (fn): Redis module. defaults to `node_redis`.

###High-level RedisClient config

`options.host` (string): Redis host url.

`options.post` (string): Redis host port.

###Low-level RedisClient config

`options.redisPub` (object): RedisClient configuration options or instance of RedisClient.

`options.redisSub` (object): RedisClient configuration options or instance of RedisClient.

`options.redisClient` (object): RedisClient configuration options or instance of RedisClient.

###Custom message packing

`options.pack` (fn): Packing mechanism. defaults msgpack if installed, otherwise `JSON.stringify`.

`options.unpack` (fn): Unpacking mechanism. defaults msgpack if installed, otherwise `JSON.parse`.
