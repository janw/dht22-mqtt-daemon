DHT22 MQTT Daemon

DHT22 MQTT is a simple daemon to query the local temperature sensor on a Raspberry Pi, and send the data to an MQTT server (in my case an embedded one from [Home Assistant](https://home-assistant.io/). It can be configured to match personal needs using the `config.ini` file, and can be daemonized using standard shell foo.

Before using it, it's dependencies have to be installed, most notably the Adafruit DHT Library. They're all inside the `requirements.txt`, and require **Python2**!

```bash
sudo apt-get install build-essential python-dev python-openssl
sudo pip install -r requirements.txt
```

Make sure to run the daemon as root (required to access the Raspberry Pi's GPIO pins):


```bash
sudo python2 mqtt-dht.py &
```
