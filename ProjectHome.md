ManyBrain Java Memcached client built for speed and high-scalability. Takes significant advantage of multi-core systems. Peak performance on loopback network at about number\_of\_threads = number\_of\_cores+2 (highly approximate). Throughput loss is gradual tested up to 500 threads. For real networks (with notably more latency than loopback) a few thousand threads should perform well (of course use, -Xss96k or so)

Very high performance for string and small payloads because of streamlined code. Large payloads (i.e., big hashmaps) still benefit, but less so as the Java serialization mechanism is a serious bottleneck.

This API is BETA and is not feature complete (yet). Notably, CAS is not supported.