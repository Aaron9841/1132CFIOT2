# 1132CFIOT2
- This implementation requires the server and database functions provided by XAMPP, combined with the temperature and humidity data read by the ESP32 used in CFIOT1, which will be transmitted back to the database.
## Hardware
First, you need those hardware to construct the environment.
- ESP32 * 1
- DHT11 * 1
- Dupont Line * 3
- USB to micro-USB wire * 1
## Software
Second, you need install some software to edit program:
- CH340 driver, for ESP32 connection.
- https://sparks.gogo.co.nz/ch340.html?srsltid=AfmBOopeMyIpntt-46BPMjZertXuS-KKUvQsJpbVBHTczKQMsF7IC7ft
- Arduino IDE, program development environment.
- https://www.arduino.cc/en/software/
- Visual Studio Code, for a better programming experience, it is recommended to download.
- https://code.visualstudio.com/download
- XAMPP, which have local server and database, we use it for contain our's data.
- https://www.apachefriends.org/download.html
> [!CAUTION]
> XAMPP will suggest you install in dask C, just follow the instruction.
### Hardware wiring diagram
By the code in Arduino, the pin have been setted.  
![image](pic/hardware.drawio.png)  
### Software setting
We start from Arduino IDE:
- Add ESP32 board
![image](https://github.com/iiotntust/1132CFIOT/blob/9df78bd0296d513af6e96ff781f7df2f19e42dce/pic/pic1.jpg)  
- Add library  
![image](pic/DHT_library.png)  
