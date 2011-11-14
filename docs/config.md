RedisStore Configuration
===

== `RedisStore([options])`

```javascript
io.configure(function () {
  io.set('store', new RedisStore({ host: 'http://redis.example.com' }))
})
```

== `options` parameters

    `options.nodeId` (string|fn): string or id generator function. default will generate unique id.

    `options.redis` (fn): Redis module. defaults to `node_redis`.

    `options.host` (string): Redis host url.

    `options.redisPub` (object): RedisClient configuration options or instance of RedisClient.

    `options.redisSub` (object): RedisClient configuration options or instance of RedisClient.

    `options.redisClient` (object): RedisClient configuration options or instance of RedisClient.

    `options.pack` (fn): Packing mechanism. defaults msgpack if installed, otherwise `JSON.stringify`.

    `options.unpack` (fn): Unpacking mechanism. defaults msgpack if installed, otherwise `JSON.parse`.
