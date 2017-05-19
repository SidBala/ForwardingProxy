# A Simple connection Forwarder

Place your proxy on a machine with two interfaces - one with access to the public internet and another with access to the private instance.

Then run ForwardingProxy

```
Usage   : ./ForwardingProxy BindAddress:Port ServerPrivateIP:Port
Example : ./ForwardingProxy 0.0.0.0:1337 10.152.0.128:1337
```