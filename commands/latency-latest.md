The `LATENCY LATEST` command reports the latest latency events logged.

Each reported event has the following fields:

* Event name.
* Unix timestamp of the latest latency spike for the event.
* Latest event latency in millisecond.
* All-time maximum latency for this event.

"All-time" means the maximum latency since the Valkey instance was
started, or the time that events were reset `LATENCY RESET`.

@examples

```
127.0.0.1:6379> debug sleep 1
OK
(1.00s)
127.0.0.1:6379> debug sleep .25
OK
127.0.0.1:6379> latency latest
1) 1) "command"
   2) (integer) 1405067976
   3) (integer) 251
   4) (integer) 1001
```

For more information refer to the [Latency Monitoring Framework page][lm].

[lm]: /topics/latency-monitor
