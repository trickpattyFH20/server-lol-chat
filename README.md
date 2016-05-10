# server-lol-chat
example implementation: http://league.chat
#### node connection to League of Legends chat servers
###### working as of: 5/10/26
#### example:
```
var ChatClient = require("./core"),
    Jid = require("./core/jid"),
    client = new ChatClient({
        accountName: "",
        password: "",
        server: "NA"
    });

client.on("online", function () {
    console.log("Connected");
});

client.on("offline", function () {
    console.log("Disconnected.");
});

client.on("message", function (message) {
    console.log(message)
});

client.on("roster", function (roster) {
    console.log(roster)
});
```
###### help from the creators of:
* [node-lol-xmpp](https://github.com/pentarex/node-lol-xmpp)
* [pilt-lib-chat](https://github.com/philippwiddra/pilt-lib-chat)