# unityMQTT
A base library for MQTT messaging in Unity defining these events:

    public delegate void ReceivedMessage(string receivedtext);
    public static event ReceivedMessage OnMessage;
    public delegate void SentMessage(string receivedtext, string topic, int qos);
    public static event SentMessage OnSentMessage;
    public delegate void Connected();
    public static event Connected OnConnect;
    public delegate void Disconnected();
    public static event Disconnected OnDisconnect;

The package is based on MQTTnet (https://github.com/chkr1011/MQTTnet).

A video showing an example implementation can be found here:
https://youtu.be/tEaMaufbM2M

Caveats:
- Use at your own risk (built for testing).
- Only tested with Akamai MQTT Broker (https://developer.akamai.com/iot-edge-connect) and Mosquito by removing TLS.
- There is no option for turning off TLS from the component GUI.
- The implementation will throw some warnings since the implementation is running async methods synchronously.
