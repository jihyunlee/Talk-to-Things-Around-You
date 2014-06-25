Talk to Things Around You
=========================

<p>Talk to Things Around You is a workshop at <a href="http://itp.nyu.edu/camp2014/" target="_blank">NYU's ITP camp 2014</a> that explores possibilities of Bluetooth LE (Low Energy) in our lives. BLE technology allows us to set up iBeacons so we can listen and broadcast real time proximity based information. We will focus on setting up high quality user experiences based on these new capabilities.</p>
<p>Jihyun Lee<br/>
e. jihyun.lee@nyu.edu<br/>
t. <a href="http://twitter.com/jihyun_says" target="_blank">@jihyun_says</a><br/></p>


##Bluetooth 4.0 Low Energy (LE)

####Applications
  - Health Care: standardized
  - Sports/Fitness: heartrate monitor, shoes
  - Security: key to car, office
  - Automation: light, temperature at home
  - Entertainment: 
  - Toys: 
  - Pay Systems: secured, localized, easy to use
  - Time Services: sync all over
  - Proximity: 
  - smart lost & found — stickNFind, Tile

####BLE Modules
  - <a href="http://www.ti.com/ww/en/wireless_connectivity/sensortag/index.shtml?INTC=SensorTag&HQS=sensortag" target="_blank">TI sensor Tag</a>
  - <a href="http://estimote.com/" target="_blank">Estimote</a>
  - RedBearLab's <a href="http://redbearlab.com/bleshield/" target="_blank">BLE Shield</a>, <a href="http://redbearlab.com/blemini/" target="_blank">BLE Mini</a>, <a href="http://redbearlab.com/blendmicro/" target="_blank">Blend Micro</a>

####Compare to Classic Bluetooth
  - Without pairing
  - Reduced power consumption and cost
  - watch <a href="http://vimeo.com/97924680" target="_blank">Tom Igoe and Don Coleman's overview of Bluetooth LE</a>

####Key Terms and Concepts
  - GATT (Generic Attribute Profile)
  - ATT (Attribute Protocol)
  - Service
  - Characteristic
  - Descriptor

####Roles and Responsibilities
  - Peripheral (Server)
    - Advertise
  - Central (Client)
    - Scan
    - Connect
    - Read / Write
  - Service: Heart Rate Monitor, ...
    - Characteristic: Heart Rate Measurement
      - Type: UUID identifying the type
      - Value: Octet string with the value
      - Properties: Read, write, notify
      - Client Configuration: Notification on/off
      - Additional Descriptor
    - Characteristic: Body Sensor Location

####Support
  - iOS 5 and later
  - Android 4.3 and later
  - Windows Phone 8.1, Windows Phone 8 (no developer API)
  - BlackBerry 10
  - Linux 3.4 and later through BlueZ 5.0

####Read more
  - <a href="http://makezine.com/2014/06/16/the-bluetooth-le-doc-a-thon-at-itp-camp/" target="_blank">Bluetooth LE Doc-a-thon</a> at <a href="http://itp.nyu.edu/camp2014/" target="_blank">ITP camp</a>
  - <a href="https://learn.adafruit.com/introduction-to-bluetooth-low-energy" target="_blank">Intro to Bluetooth Low Energy from Adafruit</a>
  - <a href="http://developer.android.com/guide/topics/connectivity/bluetooth-le.html" target="_blank">Bluetooth Low Energy from Android Developers</a>
  - <a href="http://en.wikipedia.org/wiki/Bluetooth_low_energy" target="_blank">Bluetooth Low Energy from Wikipedia</a>
  - <a href="https://developer.apple.com/videos/wwdc/2012/" target="_blank">Core Bluetooth 101 from Apple's WWDC 2012</a>


##Make Things
- <a href="https://itp.nyu.edu/physcomp/Labs/DigitalInOut" target="_blank">Arduino + LED (Digital In/Out)</a>
- <a href="https://itp.nyu.edu/physcomp/Labs/AnalogIn" target="_blank">Arduino + potentiometer (Analog In)</a>
- <a href="http://arduino.cc/en/reference/firmata" target="_blank">Arduino Firmata</a>


##Talk to Things
- Add Bluetooth LE module (ex. <a href="https://www.adafruit.com/products/1697" target="_blank">Bluefruit LE</a>) on the Arduino
  - <a href="https://learn.adafruit.com/getting-started-with-the-nrf8001-bluefruit-le-breakout/hooking-everything-up" target="_blank">Wire up</a>
  - Download <a href="https://github.com/adafruit/Adafruit_BLEFirmata" target="_blank">Adafruit_BLEFirmata Library</a>
  - Upload <a href="https://github.com/adafruit/Adafruit_BLEFirmata" target="_blank">Adafruit's StandardFirmata</a> example sketch on the Arduino
- <a href="http://phonegap.com/" target="_blank">PhoneGap</a>
  - Install
    - Install <a href="http://nodejs.org/" target="_blank">Node.js</a>
    - Run Terminal
    - <a href="http://phonegap.com/install/" target="_blank">Install PhoneGap</a>
      <pre><code>$ sudo npm install -g cordova</code></pre>
  - New Project
    - Create an App
      <pre><code>$ cordova create hello com.example.hello HelloWorld</code></pre>
    - Add platforms
      <pre><code>$ cd hello
      $ cordova platform add ios
      </code></pre>
    - List up the platforms set up for the project
      <pre><code>$ cordova platforms ls</code></pre>
    - Add Plugins
      <pre><code>$ cordova plugin add https://github.com/apache/cordova-plugin-console.git
      $ cordova plugin add https://github.com/jihyunlee/BLEFirmata.git
      </code></pre>
    - Build the App
      <pre><code>$ cordova build</code></pre>
      The cordova build command is a shortahand for the following
      <pre><code>$ cordova prepare
      $ cordova compile
      </code></pre>
    - Run the App
      <pre><code>$ cordova run</code></pre>
      But if you use multiple platform, you should declare which
      <pre><code>$ cordova run ios
      $ cordova run android</code></pre>
  - Update/Edit Project
    - Make changes
    - Build the App
      <pre><code>$ cordova build</code></pre>
    - Run the App
      <pre><code>$ cordova run</code></pre>


###References
- <a href="https://itp.nyu.edu/physcomp/Intro/HomePage" target="_blank">NYU ITP's Intro to Physical Computing</a>
- <a href="http://docs.phonegap.com/en/3.5.0/guide_cli_index.md.html#The%20Command-Line%20Interface" target="_blank">PhoneGap's Command Line Interface</a>
- http://www.slideshare.net/EVRYTHNG/android-the-web-of-things-bluetooth-low-energy-bluetooth-40-ibeacons-barcodes-qrs-nfc-arduino
- http://www.instructables.com/id/Talk-to-an-Arduino-With-an-iOS-device-using-Blueto/?ALLSTEPS
- http://beekn.net/2014/05/ibeacon-and-wwdc-3-things-to-watch/
