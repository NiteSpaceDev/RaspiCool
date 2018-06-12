# Project setup
This project is in early development and process may change dramatically.   Migration steps may not be obvious.
Long term project will include an SD Card image with software pre-buit and installed.

# Hardware Prerequisites
* Raspberry Pi (Development currently on Pi 3b+)
  * Expected HW needs:
    * Dual mode capable wifi - Pi is an AP for the sensors
    * Bluetooth - This will be used to register the sensors
    * MicroSD Card - Size will affect how much sensor data can be stored (stats pending)
      * Currently using 64G card in dev
      * Expected minimum 8G
* ESP32 based sensor(s) - see (https://github.com/NiteSpaceDev/raspicool-environment-sensor)

# Manual Software setup 
1  Start by flashing Raspbian Stretch Lite and boot Pi, connect to network normally
2  Install Docker 
   - curl -fsSL https://get.docker.com/ | sudo sh
3  Setup Swarm
   - docker swarm init --advertise-addr 127.0.0.1
4  Create Docker networks for service separation
   - Database network for containers that talk to Timescale
5  Build TimescaleDB container image
6  Start Timescale service
7  Start MQTT service (Pending)
8  Start Dataload service - Connects via MQTT to load data into Timescale
9  Start Cloud data relay (Pending)
10 Start Dashboard web server (Pending)
11 Start Touch screen interface (Embedded web client w/ built-in auth) (pending)
