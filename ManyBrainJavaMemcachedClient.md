# Introduction #

All user facing calls are in MemCacheClient.java

Use is pretty straightforward, create the client with the servers, ports, and weights.

String servers = new String[.md](.md) { "server1.com:3993", "server2.com: 8833" };
int weights = new int[.md](.md) { 3, 6 };
MemCacheClient mcc = new MemCacheClient(servers, weights };

Then call set/get.

mcc.set("TheKey", "The value is right here dude");
mcc.set("TheBigObject", map);

String v = mcc.get("TheKey");

# Hashing #

The current hashing mechanism is custom but is consistent. If you require compatibility with an existing hashing system, then this probably isn't for you (or you could plug it in).