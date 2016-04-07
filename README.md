# qwerk_reboot
rebooting an old but powerful relic

After many coffees, lattes and hot cocoas...
some quick notes on rebooting the old but powerful CharmedLabs' Qwerk board!

If anyone has info to add in, please let me know! Thank you.

A quick overview of Qwerk’s hardware features:
· 200 MHz ARM9 RISC processor with MMU and hardware floating point unit
· 32 Mbytes SDRAM, 8 Mbytes flash memory
· 4 closed-loop 2.0 Amp motor controllers (supports quadrature encoder and back-EMF “sensorless” position feedback as well as
current sensing)
· 16 RC-servo controllers
· 16 programmable digital I/Os
· 8 12-bit analog inputs
· 2 RS-232 ports
· I2C ports
· 2 USB 2.0 host ports for connecting standard USB PC peripherals
· 10/100BT Ethernet port
· Built-in audio amplifier with MP3, PCM and WAV audio support
· 4 Amp switching power supply, 90% efficient, 7 to 30 Volt input range
· Rugged aluminum enclosure
· 5.1” x 5.8” x 1.3”, 12.8 ounces

POWER
Input Voltage (max): 34.0V
Input Voltage (min):  7.0V
** If you've lost your Molex connector and need a way to connect power again:
Molex 2.36x22 mm female crimps (solder wires yourself)
I got mine from Sayal Electronics in Canada but I'm sure Digikey/Mouser etc. will also sell them
Pinout ('circle' | 'AND gate-shape') or 'Pin2' | 'Pin1'): POWER + GND
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
<To-do>

Other Resources:
1. See datasheets folder
2. https://sourceforge.net/projects/terk/ (Terk firmware and ARM compiler available)
2. Via Wayback Machine: https://web.archive.org/web/20110713065937/http://www.terk.ri.cmu.edu/
