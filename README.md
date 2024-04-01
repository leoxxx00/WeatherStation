# Raspberry Pi DHT22/DHT11 Weather Station 
A DHT22/DHT11 Weather Station project using Python, Flask, Flask-SocketIO, and Bootstrap that displays real-time temperature and humidity sensor readings of your multiple sensors on Raspberry Pi
Original- https://github.com/donskytech/dht22-weather-station-python-flask-socketio-multiple-sensors.git  
NOTE!!!! Use Thunderbirds Teams's reengineered version of the Original project for flask LAN connections. Combined with a remote solution by using remote it. full framework credit to Donkeytech.
## Steps on how to run on Raspberry Pi
1. Clone the repository
```
git clone https://github.com/leoxxx00/WeatherStation.git
cd WeatherStation/
```
2. Create a Python virtual environment
```
python -m venv .venv
source .venv/bin/activate
```
3. Install the dependencies
```
pip install -r requirements.txt
```

4. Run the application
```
flask run --host=0.0.0.0
```
5. Access the application using the following URL
```
http://<IP>:5000
```
### How to add multiple DHT22/DHT11 sensors
Edit your app.py and add the new variables like the below code
  
```
dht22_module_1 = DHT22Module(1, board.D2)
dht22_module_2 = DHT22Module(2, board.D3, adafruit_dht.DHT11)
dht22_module_3 = DHT22Module(3, board.D4)
dht22_module_4 = DHT22Module(3, board.D17)
dht22_module_5 = DHT22Module(3, board.D27)
dht22_module_6 = DHT22Module(3, board.D22)

dht_modules = [dht22_module_1, dht22_module_2, dht22_module_3, dht22_module_4, dht22_module_5, dht22_module_6]
```
This would add 3 more additional sensor on your web application  
```
###also pip install flask-cors on resberry pi
```
### To auto-start this project  
https://www.donskytech.com/raspberry-pi-how-to-start-python-script-on-boot/
```
##To make this project remote 
go to there- https://app.remote.it
register your pi inside Raspberry pi by copy paste on the terminal
go to SSH and type in pi's local IP on the service host and the port number in the service port
give any name you like on the service name
Next, go to remote.it and connect the host on the connections
copy the PUBLIC ENDPOINT and enjoy
if lost, follow 9:56 on this https://youtu.be/i9mJzdLYsVo?si=gZNnWt0LrpoSxjl-
```
### Also, if the git is not clonable, you can download the files manually and run the file inside the folder of your path.
```
