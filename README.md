# Radiosys@Term

**This is an executable file which is working on Windows 8 later.**

</br>
<img width="1125" height="903" alt="about_Radiosys@Term" src="https://github.com/user-attachments/assets/79d368c6-73ab-40d4-9654-e08c0cb970c4" />
</br>
</br>
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

**RX TIMEOUT?**\
It depens on the baudrate settings. In MODBUS side, it accepts 3.5 bytes of leadout delay though. this terminal waits and terminates a packet stream in 64 bytes timeout plus 10ms. I have tried to set this terminal with much shorter Rx timeout value such as 3.5 bytes in the main thread...but, it was not accurate. because of my poor skill ???
if a device streams out a packet within the above value as the inter byte delay, they would be regarded as one string. a packet always starts from ">". it means your packet is not a string if you can see ">" in the middle of a packet and it was not a intended char.

**COMM WINDOW**\
You can toggle between ASCII and HEX. a hex char is displayed by the format of "XX:" (two digits + colon). the characters beyond ASCII table will be displayed in the above manner even though you set it at ASCII mode.
eg.: "8B:88:34" means "0x8B 0x88 0x33 9x34"

**TRASMIT LINE**\
You can set "EOL" (end of line) to terminate a string in "NONO", "CR", "LF", "CR+LF". or "CR" will be followed by your string if you press "Enter" key.

There is a special char "$". you can use "$XX to send a hexdecimal char. and you have to use "$$" in order to send a real "$" character.

example 1.
abcdefgh123456 - this will send "abcdefgh123456"
example 2.
$$123 - this will send "$123"
example 3.
$01$02$03$04$05 - this will send 0x01 0x02 0x03 0x04 0x05

**HOW TO USE TX MULTI FUNCTION?**\
You can send a predefined string in each TX MULTI FUNCTION, totally twenty four (24). and you can set it periodic repeative timer. by the way, please be cautious to set up a right timer value depending on the length of packet and the baudrate you set up. and each TX MULTI FUNCTION has got same characteristic as one of the transmit line.

**VIRUS CHECKUP**\
I don't know why they suspect Radiosys@Term malicious. Windows Security often warns you it as a malicious app.



</br>
<img width="1630" height="1072" alt="about_Radiosys@Term_info" src="https://github.com/user-attachments/assets/bd418773-0c8d-4d41-8c13-79bea6105cea" />
</br>
</br>

**CONTACT**\
feel free to contact jnlee4838@gmail.com
</br>
</br>
**High Speed Isolated USB to Serial Converter Modules**\
</br>
I was often in trouble to make the serial work properly whenever kick off new projects cause uart is the very first step.
</br>
I have decided to make some converter modules which support high speed and isolation in both signal and power.
</br>
</br>
**1. High Speed Isolated USB to UART Converter Module 6Mbps 5kV**\
</br>
<img width="2400" height="2400" alt="top High Speed Isolated USB to UART Converter Module 6Mbps 5kV" src="https://github.com/user-attachments/assets/5292397d-afcb-4d21-90a2-19b97bb4c019" />
<img width="2400" height="2400" alt="bottom High Speed Isolated USB to UART Converter Module 6Mbps 5kV" src="https://github.com/user-attachments/assets/e025799c-b010-40f8-9097-d3bd7d082c17" />
</br>
Buy: https://smartstore.naver.com/radiosystek/products/12396782235
</br>
</br>
</br>
**2. High Speed Isolated USB to 485T Converter Module 250kbps 5kV**\
</br>
<img width="2400" height="2400" alt="top High Speed Isolated USB to 485T Converter Module 250kbps 5kV" src="https://github.com/user-attachments/assets/6da549be-806c-4e1b-9bde-ff3d1428bc9a" />
<img width="2400" height="2400" alt="bottom High Speed Isolated USB to 485T Converter Module 250kbps 5kV" src="https://github.com/user-attachments/assets/2cceec9c-c0d8-4f6e-9db8-9c2aaedcb301" />
</br>
Buy: https://smartstore.naver.com/radiosystek/products/12405048497
</br>
</br>
</br>
</br>

