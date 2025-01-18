# network code

Well going from 2 players to 4 players or more
means that I have to dive into the network code.

So looking into `src/js/core/network.js` ...

peer.js is handling the network stuff



How data is revieved and processed:
* peer.on('connection', ...)
    * `peerConnection = conn;` : a single connection ??
    * calls processData(data)

```
const params = [text, gamePrefs.net_player_name];
net.sendMessage({ type: 'CHAT', params });
```

Actions:
* let peerConnections[]
* peerConnections.push(connection) on connection.on('open')



TODO:
* `connection.on('close'` close only one connection, if everyone disconnect thet reset
* `sendMessage` update ??
* `sendDelayedMessage` update ??
* look for console message `remote ready; starting game immediately`
* look for console message `local is ready; delaying, then starting game 1.5`
* look for console message `NETWORK GAME`
* look for console message `you are hosting: you are helicopters[0], and take the friendly base`
* see messageActions
* see preferences.js `gamePrefs.net_player_name`

# log

* 2025-01-18: chat is working one way (server > client) for 3 players
