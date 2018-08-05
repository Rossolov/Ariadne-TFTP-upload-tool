# Ariadne-TFTP-upload-tool

Program is used for download firmware to devices with Ariadne bootloader https://github.com/per1234/Ariadne-Bootloader
TFTP client from http://www.tftp-server.com/tftp-download.html

Created in Hiasm http://hiasm.com/

Using the program:
1. locate firmware HEX file
To do that, first set File > Preferences > Show verbose output during compilation(check) in the Arduino IDE and then click the Verify button. This will convert your sketch into a .hex file located in a temporary folder. The location of the temporary folder is printed in the last line of the compilation output. For example:

C:\Program Files (x86)\Arduino\hardware\tools\avr/bin/avr-objcopy -O ihex -R .eeprom C:\Users\username\AppData\Local\Temp\build4255864821845399166.tmp/sketch/Blink.cpp.elf C:\Users\username\AppData\Local\Temp\build4255864821845399166.tmp/sketch/Blink.cpp.hex
Enter the directory and make sure that there is a .elf or a .hex file with the same name as your sketch.

2. Set IP address of the device with Ariadne bootloader

3. Reboot the device just before pressing UPLOAD button to enable bootloader.

4. Upload firmware
