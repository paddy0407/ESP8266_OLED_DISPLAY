# ESP8266_OLED_DISPLAY
Using an ESP8266 and an I2C OLED display, this will be able to remotely display a message sent from the local network through a browser

This requires an ESP8266 and an OLED I2C Display
I used a 0.91" I2C display

Variables that need set in sketch:
Depending on display type: 
Under Start send to displaay
The line:
  display.begin(SSD1306_SWITCHCAPVCC, 0x3C);
Ox3C is for the 128x32 displays (0.91")
Ox3D is used for the 128x64 displays (0.96")

To send a message to display, the IP showing on the display after flashing should be used in the following:

http:192.168.1.141/messge?msg=TESTING

Scripts can then be automated to send messages to this address with the address being variable

This has been done for the pssiblity to be used along with Home Assistant and the RESTful component

