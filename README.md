# A Simple connection Forwarder


Normally we have:
sequenceDiagram
    participant Client
    participant Forwarder
    participant PublicServer

    Client->>PublicServer: Connect
    PublicServer->>Client: Accept

when PublicServer is not public, we cannot connect.

With ForwardingProxy:
sequenceDiagram
    participant Client
    participant Forwarder
    participant PrivateServer
    Client->>ForwardingProxy: Connect
    ForwardingProxy->>PublicServer: Connect
    PublicServer->>ForwardingProxy: Accept
    ForwardingProxy->>Client: Accept

```
Usage   : ./ForwardingProxy BindAddress:Port ServerPrivateIP:Port
Example : ./ForwardingProxy 0.0.0.0:1337 10.152.0.128:1337
```