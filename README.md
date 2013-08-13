nRF24AP2_SUART
==============

Nordic nRF24AP2 (ANT+) UART module interface for Arduino using SoftwareSerial (software UART).

This code was to determine and test the interface of a cheap Nordic nRF24AP (ANT+) UART module from Goodluckbuy (and various other places) and documenting the details.

This module, marked with "NRF24AP2 YJ-ANT", lacks any documentation.....
http://www.goodluckbuy.com/nrf24ap2-networking-module-zigbee-module-with-ant-transceiver-.html
(and very likely [not tested] http://www.goodluckbuy.com/nrf24ap2-wireless-module-zigbee-module.html  )

Also appears to be at: http://www.aliexpress.com/store/product/Freeshipping-NRF24AP2-Wireless-Networking-Module-Zigbee-Module/809689_559703297.html

The outcome of the testing is:

The connector on the module is (looking from the front, pin 1 is marked []) has

[]GND(=VSS) | VDD(=3.3 volts)

UART_TX   | UART_RX

!(SUSP)   | SLEEP

RTS       | !(RESET)

Baud rate of the module is 9600 bps.


Output
==============
nrf24AP2 Tester!

Setup() Complete!

Received RTS Interrupt. We are CTS (ANT is ready to receive again).

Wait...

RECV:0xA416F814B.

Hardware RESET

Received RTS Interrupt. Waiting for ANT to let us send again.

Wait...

RECV:0xA416F1CB.

RESET_SYSTEM()

RECV:0xA416F20EA.

Received RTS Interrupt. We are CTS (ANT is ready to receive again).

Wait...

REQUEST( CAPS )

RECV:0x33A285348489B1350EF.

Received RTS Interrupt. We are CTS (ANT is ready to receive again).

Wait...

That's all folks!!! [Aborting to exit.]
