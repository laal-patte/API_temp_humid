**Task 1:** Make an drag-n-drop mobile app with web based api to get temperature and humidity data.

**Task 2:** Make a flask app in raspberry pi to show temperature and humidity data coming from sensor on localhost.

### Setting up raspberry pi on your pc

1. Need to download and setup VNC viewer [Download](https://www.realvnc.com/download/file/viewer.files/VNC-Viewer-6.19.325-Windows.exe)
    - In this we'll view pi's screen.
2. Connect raspberry pi with power supply and with ethernet to your computer.
3. Open VNC viewer and type IP given on the slip, connect with username: pi and password: raspberry.

---

### Running temperature+humidity sensor

1. Connect sensor to raspberry pi as showed in [picture](http://www.circuitbasics.com/wp-content/uploads/2015/12/How-to-Setup-the-DHT11-on-the-Raspberry-Pi-Three-pin-DHT11-Wiring-Diagram.png)
    - make sure that connections - vcc:pin2, gnd:pin5, data:pin8
2. Run the following commands :
    - getting git :
          
          sudo apt-get update
          sudo apt-get install build-essential python-dev python-openssl git
    - getting liberary for sensor :
          
          git clone https://github.com/adafruit/Adafruit_Python_DHT.git && cd Adafruit_Python_DHT
          sudo python setup.py install
          cd examples
    - To see the temperature :
          
          sudo ./AdafruitDHT.py 11 4       
 
 ### Mobile app
 
 * [appsgeyser.com](https://www.appsgeyser.com/create/start/)
    - choose website -> put google.com -> (create)+signup using google -> goto edit/tabs -> add tab>html -> write your code there..

### REST api call

* link : http://api.openweathermap.org/data/2.5/weather?q=__city_name__&units=metric&appid=__api_id__
* api_id : *5a45632ef38d7166a8422ff43684b661*
* units :
    - units=metric : Celsius
    - units=imperial : Fahrenheit
    - default : kelvin
