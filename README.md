SocketIo4Netty
=======================

SocketIo4Netty is a simple [Socket.IO](http://socket.io) Java server implementation based on 
[Netty](http://netty.io) server framework. Supports 0.7+ up to latest 0.9.12 versions of 
Socket.IO-client.

Supported transport protocols:
* WebSocket
* XHR-Polling 

How to use
-----------------------

``` java
	SocketIOServer socketIoServer = new SocketIOServer();
	socketIoServer.setPort(5000);
	socketIoServer.setListener(new SocketIOAdapter() {
		public void onMessage(ISession session, String message) {
			System.out.println("Received message: " + message);
		}
	});
	socketIoServer.start();
```

For more examples, see [socketIo4Netty-examples](https://github.com/socketIo4Netty/socketIo4Netty-examples). 

Maven
----------------------

``` maven
<dependency>
	<groupId>com.github.socketIo4Netty</groupId>
	<artifactId>socketIo4Netty</artifactId>
	<version>1.0.10</version>
</dependency>
```