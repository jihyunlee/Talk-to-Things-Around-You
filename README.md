Talk to Things Around You
=========================

<p>Talk to Things Around You is a workshop at <a href="http://itp.nyu.edu/camp2014/" target="_blank">NYU's ITP camp 2014</a> that explores possibilities of Bluetooth LE (Low Energy) in our lives. BLE technology allows us to set up iBeacons so we can listen and broadcast real time proximity based information. We will focus on setting up high quality user experiences based on these new capabilities.</p>
<p>Jihyun Lee<br/>
e. jihyun.lee@nyu.edu<br/>
t. <a href="http://twitter.com/jihyun_says" target="_blank">@jihyun_says</a><br/></p>


Bluetooth 4.0 Low Energy (LE)
--------
- Examples
  - Health Care
  - Sports/Fitness
  - Security
  - Automation
  - Entertainment
  - Toys
  - Pay Systems
  - Time Services
  - Proximity

- GATT (Generic Attribute Profile)
  - Central (Client)
    - Scan
    - Connect
    - Read/ Write
  - Peripheral (Server)
    - Advertise
      - Service: Heart Rate Monitor, ...
        - Characteristic: Heart Rate Measurement
          - Type: UUID identifying the type
          - Value: Octet string with the value
          - Properties: Read, write, notify
          - Client Configuration: Notification on/off
          - Additional Descriptor
        - Characteristic: Body Sensor Location


Make Things
-----------
- <a href="https://itp.nyu.edu/physcomp/Labs/DigitalInOut" target="_blank">Arduino + LED (Digital In/Out)</a>
- <a href="https://itp.nyu.edu/physcomp/Labs/AnalogIn" target="_blank">Arduino + potentiometer (Analog In)</a>
- <a href="https://itp.nyu.edu/physcomp/Labs/SerialOut" target="_blank">Serial communication</a>


Talk to Things
--------------
- add BLE module (ex. <a href="https://www.adafruit.com/products/1697" target="_blank">Bluefruit LE</a>
- <a href="http://phonegap.com/" target="_blank">PhoneGap</a>
  - Install
    - Install <a href="http://nodejs.org/" target="_blank">Node.js</a>
    - Run Terminal
    - <a href="http://phonegap.com/install/" target="_blank">Install PhoneGap</a>
      <pre><code>$ sudo npm install -g cordova</code></pre>
  - New Project
    - Create an App
    - Add platforms
    - Add Plugins
    - Build the App
    - Run the App
  - Update/Edit Project
    - Make changes
    - cordova prepare
    - Clean Build
    - Build the App
    - Run the App
