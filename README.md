
# Serial Terminal - Radiosys@Term

Another serial terminal in MS Windows 8 later...

It is an exe file, no source code.

This terminal is inspired by Br@y Terminal. by the way. Thanks to Bray!

## Updated V0.0.5

* **Resize**: Resizable and COMM window will be enlarged.
* **Font & Font Size**: the font is changed to "Arial Narrow" 10pt & another font in COMM window has been changed to "Arial" 11pt for better discrmination.

![Radiosys@Term Serial Terminal](/images/Radiosys@Term_serial_terminal_0_5.png)

* easy to use.

* ASCII or HEX transmission.

* ASCII or HEX receiption.

* Differet color in transmission and receiption.

* DTR & RTS controllable.

* Twenty four (24) macros for transmission.



## Usage/Examples


### Rx Timeout

It depends on the baudrate settings.

In MODBUS side, it accepts 3.5 bytes of leadout delay though.

This terminal waits and terminates a packet stream in 64 bytes timeout plus 10ms.

I have tried to set this terminal with much shorter Rx timeout value such as 3.5 bytes in the main thread...but, it was not accurate.
because of my poor skill ???

If a device streams out a packet within the above value as the inter byte delay, they would be regarded as one string.

A packet always starts from ">".

it means your packet is not a string if you can see ">" in the middle of a packet and it was not a intended char.


### Comm Window

You can toggle between ASCII and HEX.

A hex char is displayed by the format of "XX:" (two digits + colon).

The characters beyond ASCII table will be displayed in the above manner even though you set it at ASCII mode. eg.: "8B:88:34" means "0x8B 0x88 0x33 9x34"


### Transmission

You can set "EOL" (end of line) to terminate a string in "NONO", "CR", "LF", "CR+LF". or "CR" will be followed by your string if you press "Enter" key.

There is a special char "**$**". you can use "$XX to send a hexdecimal char. and you have to use "$$" in order to send a real "$" character.

* example 1. abcdefgh123456 - this will send "abcdefgh123456".

* example 2. $$123 - this will send "$123".

* example 3. $01$02$03$04$05 - this will send 0x01 0x02 0x03 0x04 0x05.


### Macro

You can send a predefined string in each macro(Tx Multi Function), totally twenty four (24).

You can set it periodic repeative timer. by the way, please be cautious to set up a right timer value depending on the length of packet and the baudrate you set up.


### Virus check

I don't know why they suspect Radiosys@Term malicious. Windows Security often warns you it as a malicious app.

![Radiosys@Term Virus Total check](/images/Radiosys@Term_virus_total_check.png)

**It's Not !!!**


## Support

For support, [**email me**](jnlee4838@gmail.com)


