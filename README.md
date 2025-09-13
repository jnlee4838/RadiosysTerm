# Radiosys@Term

This is an executable file which is working on Windows 8 later.

<img width="1125" height="903" alt="about_Radiosys@Term" src="https://github.com/user-attachments/assets/79d368c6-73ab-40d4-9654-e08c0cb970c4" />

Thie terminal is inspired by Br@y Terminal. by the way. Thanks to Bray

DB9 PINOUT on PC:
1 - CD - Carrier Detect (IN)
2 - RX - Data Receive (IN)
3 - TX - Data Transmit (OUT)
4 - DTR - Data Terminal Ready (OUT)
5 - GND - Ground
6 - DSR - Data Set Ready (IN)
7 - RTS - Request To Send (OUT)
8 - CTS - Clear To Send (IN)
9 - RI - Ring Indicator (IN)

RX TIMEOUT?
It depens on the baudrate settings. In MODBUS side, it accepts 3.5 bytes of leadout delay though. this terminal waits and terminates a packet stream in 64 bytes timeout plus 10ms. I have tried to set this terminal with much shorter Rx timeout value such as 3.5 bytes in the main thread...but, it was not accurate. because of my poor skill ???
if a device streams out a packet within the above value as the inter byte delay, they would be regarded as one string. a packet always starts from ">". it means your packet is not a string if you can see ">" in the middle of a packet and it was not a intended char.

COMM WINDOW
You can toggle between ASCII and HEX. a hex char is displayed by the format of "XX:" (two digits + colon). the characters beyond ASCII table will be displayed in the above manner even though you set it at ASCII mode.
eg.: "8B:88:34" means "0x8B 0x88 0x33 9x34"

TRASMIT LINE
You can set "EOL" (end of line) to terminate a string in "NONO", "CR", "LF", "CR+LF". or "CR" will be followed by your string if you press "Enter" key.

There is a special char "$". you can use "$XX to send a hexdecimal char. and you have to use "$$" in order to send a real "$" character.

example 1.
abcdefgh123456 - this will send "abcdefgh123456"
example 2.
$$123 - this will send "$123"
example 3.
$01$02$03$04$05 - this will send 0x01 0x02 0x03 0x04 0x05

HOW TO USE TX MULTI FUNCTION?
You can send a predefined string in each TX MULTI FUNCTION, totally twenty four (24). and you can set it periodic repeative timer. by the way, please be cautious to set up a right timer value depending on the length of packet and the baudrate you set up. and each TX MULTI FUNCTION has got same characteristic as one of the transmit line.

Virus checkup
I don't know why they suspect Radiosys@Term malicious. Windows Security often warns you it as a malicious app.

<img width="1630" height="1072" alt="about_Radiosys@Term_info" src="https://github.com/user-attachments/assets/bd418773-0c8d-4d41-8c13-79bea6105cea" />

CONTACT
feel free to contact jnlee4838@gmail.com


