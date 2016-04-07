# qwerk_reboot
rebooting an old but powerful relic

After many coffees, lattes and hot cocoas...
some quick notes on rebooting the old but powerful CharmedLabs' Qwerk board!

If anyone has info to add in, please let me know! Thank you.

A quick overview of Qwerk’s hardware features:
- 200 MHz ARM9 RISC processor with MMU and hardware floating point unit
- 32 Mbytes SDRAM, 8 Mbytes flash memory
- 4 closed-loop 2.0 Amp motor controllers (supports quadrature encoder and back-EMF “sensorless” position feedback as well as
current sensing)
- 16 RC-servo controllers
- 16 programmable digital I/Os
- 8 12-bit analog inputs
- 2 RS-232 ports
- I2C ports
- 2 USB 2.0 host ports for connecting standard USB PC peripherals
- 10/100BT Ethernet port
- Built-in audio amplifier with MP3, PCM and WAV audio support
- 4 Amp switching power supply, 90% efficient, 7 to 30 Volt input range
- Rugged aluminum enclosure
- 5.1” x 5.8” x 1.3”, 12.8 ounces

POWER
- Input Voltage (max): 34.0V
- Input Voltage (min):  7.0V
- ** If you've lost your Molex connector and need a way to connect power again:
- Molex 2.36x22 mm female crimps (solder wires yourself)
- I got mine from Sayal Electronics in Canada but I'm sure Digikey/Mouser etc. will also sell them
- Pinout ('circle' | 'AND gate-shape') or 'Pin2' | 'Pin1'): POWER + GND
--> or do continuity test to determine where the ground pin is

TERMINAL
- connect via UART1 port
- Method: COMPUTER --> USB2RS232(DB9) --> QWERK:DB9 Connector (this came with your unit) --> modular cable --> QWERK
- Console connects at 57.6K, 8 data bits, 1 stop bit, no parity, no flow control
1. Turn-off Qwerk and connect to computer
2. Start your favority terminal app with the settings
3. Turn on Qwerk and it should connect
4. Hit 'Ctrl-C' to get into RedCos
5. Hit 'Enter' after everything loads to get into Linux

ETHERNET
1. Turn Qwerk off
2. Connect ethernet between unit and PC
3. Change TCP/IP (v4) to: IP address: 192.168.1.150 (subnet 255.255.255.0)
4. Hold down CFG button on Qwerk and power-on while holding down the button. Wait till all LEDs begin blinking before letting go.
5. You are now in Diagnostic Mode
6. Reset by hitting CFG 7X (LED 6 will light up followed by all LEDs blinking notifying you that you're in diagnostics menu)
7. Goto static IP mode: hit CFG 5X (LED 4 lights up)
8. Open browser and goto http://192.168.1.144
9. Qwerk's ethernet configuration page!
- General Configuration Tab:
- Network Broadcast Name: change to something you want (ie http://yournamehere)
- Client Connection Mode: switch to Direct-Connect since relay server is inactive now
- Wireless Configuration Tab: configure your settings
- Ethernet Configuration Tab:
- Use the following IP address: set your setting for your local network
- hit APPLY to save settings
10. Exit Qwerk diagnostic mode by pressing CFG 8X
11. LED 6 should blink
12. If Qwerk connects to your local network, you should see LED 0, 1, and 2 light up.


Other Resources:
1. See datasheets folder
2. https://sourceforge.net/projects/terk/ (Terk firmware and ARM compiler available)
2. Via Wayback Machine: https://web.archive.org/web/20110713065937/http://www.terk.ri.cmu.edu/
