# peltier_degeneration
Peltier system for assaying thermally induced degeneration in Drosophila.  
Designed by Jacob Jaszczak and Luke Breuer  
Built by Jacob Jaszczak

1) Install microcontroler driver. The board URC10 uses CH340G USB to UART converter. Download windows driver here: http://sparks.gogo.co.nz/assets/_site_/downloads/CH34x_Install_Windows_v3_4.zip  
For MAC and Linux, see URC10 Cytron manual. 

2) Install Arduino IDE 
https://www.arduino.cc/en/software

3) Download and copy thermocouple libraries to the "Arduino libraries" folder as subfolder "PWFusion_MAX31856"  
	2A: path example: ...\Documents\Arduino\libraries\PWFusion_MAX31856
	
	2B: Four files starting with "PlayingWithFusion_"

4) Open "thermal_degeneration.ino" code

5) Set up IDE  
	4A: Tools > Board > "Arduino Uno"
	
	4B: Tools > Port > Select port that is activated by the USB connection.
						*If port does not appear, or IDE cannot connet to the beard during upload, then trouble shoot through the manager*

	4C: Tools > Serial Monitor > Baud > "38400"

6) Edit # Assay variables # *note, time variables must be in seconds
  - targetTemp = target temperature that program is held at. 
  - beginningHold = seconds after start button is pressed before the thermal program begins.
  - holdTarget = seconds that the target temperature is held for. After hold time is complete the Peltiers will turn off, but he fans and the thermocouples will stay on. 
  - assayTime = total assay time, afterwhich the fans will shutdown and the thermocouples will stop recording. 
  
7) Upload "thermal_degeneration.ino" code to microcontroller (button with arrow). 

8) Open Serial Monitor

9) To start assay, press the START button. The LED will turn on. 

10) To stop assay at any time, press the RESET button. This will reload the code in the microcontroller and reset all variables. 

11) Save Serial Monitor data by copy all (control + A) and paste (control + c) into a Notepad file

12) Reset Serial Monitor with the "clear" button before beginning another assay 
