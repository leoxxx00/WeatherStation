# Raspberry Pi DHT22/DHT11 Weather Station 
A DHT22/DHT11 Weather Station project using Python, Flask, Flask-SocketIO, and Bootstrap that displays real-time temperature and humidity sensor readings of your multiple sensors on Raspberry Pi
Original- https://github.com/donskytech/dht22-weather-station-python-flask-socketio-multiple-sensors.git  
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

###also pip install flask-cors on resberry pi
  
### To auto-start this project  
https://www.donskytech.com/raspberry-pi-how-to-start-python-script-on-boot/
