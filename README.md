This is a full repository of code referenced in my 3rd year project report.

There are 5 files in this repository, four marked 'Arduino' which are written in C++, and one marked 'MATLAB' which is written in Matlab code.

To run arduino code, simply download the Arduino IDE, plug in the microcontroller, paste the code included in the relevant file, and press the run button in the IDE. 
All sketches use the serial monitor, which can be accessed through the 'tools' menu in the IDE, to see printed messages used for debugging and data collection
Some sketches use a different baud rate defined in the line "Serial.begin(9600);". Ensure that the serial monitor's rate matches the rate defined in the script, otherwise printed messages will not be readable
Some sketches include external libraries. These can be installed by opening the library manager page in the IDE, and searching for the necessary library, then installing it.

The file 'Arduino presaved SD datalogger' is one of the 'example projects' that comes preloaded in the Arduino IDE. It was used as inspiration at the start of the process for creating SD card writing capabilities in my code

The file 'Arduino RTC basic testing' contains code taken from https://RandomNerdTutorials.com/arduino-ds3231-real-time-clock/ which was used to test the real time clock module.

The file 'Arduino filter testing' contains the code used to generate figures _ in section 3.3 of the report, with the key functionality explained in figure_
The exponential smoothing algorithm used is given by yn = x+(1-)yn-1
The code in it's current state has a bug where it can sometimes suffer from steady state error. This is being tested and addressed.
The code contains AI generated snippets and these are marked

The file 'Arduino SD card full program' contains the code used to write files to an SD card, such as that in figure_ in section 3.3 of the report.
This code combines the functionality of the two previous files, and relevant lines are referenced from where they have been taken.
The code contains AI generated snippets and these are marked

The file 'MATLAB data presentation' contains the code that was used to generate all MATLAB graphs in the report (Figures ___)
After downloading the MATLAB app, the code is run by simply pasting it into the editor and pressing the 'run' button.  The function of the code is explained in figure _
To read data from a file, the user must set a filepath to the folder where they will keep .txt files with data in. 
Once the filepath is set up, simply move the .txt data file into the folder and change line 3 to "rawdata = fileread("your_file.txt");"
The script will only read data with the structure: 
- data begins after the phrase "data follows;"
  - data is of the format 'time,data1,data2,time,data1,data2...'
If the user's data does not follow this format, then change line 4 for the initial delimiter, line 6 for the data delimiters, and lines 11-14 for a different number of data points being sent per group.
  Line 16 will also need to be changed to the variable name for the last datapoint of the group
The code contains AI generated snippets and these are marked


