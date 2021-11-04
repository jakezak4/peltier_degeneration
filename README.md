# peltier_degeneration
Peltier system for assaying thermally induced degeneration in Drosophila

1) Install Arduino IDE 
https://www.arduino.cc/en/software

2) Download and copy thermocouple libraries to the "Arduino libraries" folder as subfolder "PWFusion_MAX31856"  
  2A) path example: ...\Documents\Arduino\libraries\PWFusion_MAX31856

3) Open "thermal_degeneration.ino" code

4) Set up IDE
  4A) Tools > Board > "Arduino Uno"
  4B) Port > *Select port that activated by the USB connection* 
             *If port does not appear, or IDE cannot connet to the beard during upload, then trouble shoot through the manager*
  4C) Serial Monitor > Baud > "38400"

5) Edit # Assay variables #

  targetTemp = target temperature that program is held at 
  beginningHold = seconds after start button is pressed before the thermal program begins   
  holdTarget = seconds that the target temperature is held for
  assayTime = total assay time, afterwhich the Peltiers with shutdown but the fans will remain on 

  *note, time variables must be in seconds

6) Upload "thermal_degeneration.ino" code to microcontroler (button with arrow). 

7) Open Serial Monitor

8) To start assay, press the START button. The LED will turn on. 

9) To stop assay at any time, press the RESET button. This will reload the code in the microcontroler and reset all variables. 

10) Save Serial Monitor data in by copy all (control + A) and paste (control + c) into Notepad 

11) Reset Serial Monitor with the "clear" button before begining another assay 
