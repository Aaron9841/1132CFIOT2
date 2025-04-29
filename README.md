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
> XAMPP will suggest you don't install in C:\ or C:\Program Files(x86), just follow the instruction.
### Hardware wiring diagram
By the code in Arduino, the pin have been setted.  
![image](pic/hardware.drawio.png)  
### Software setting
#### Arduino
We start from Arduino IDE:
- Add ESP32 board
![image](https://github.com/iiotntust/1132CFIOT/blob/9df78bd0296d513af6e96ff781f7df2f19e42dce/pic/pic1.jpg)  
- Add library  
![image](pic/DHT_library.png)  
#### XAMPP
And then we start to deal with XAMPP:
> [!WARNING]
> We only need to use the functions highlighted in the red box; the others can be unchecked.  
> ![image](pic/XAMPP_1.png)  

- FileZilla FTP Server: Used for file transfer; this is required if users need to upload or download files.  
- phpMyAdmin: A graphical user interface for managing MySQL databases.  
- Webalizer: A program for recording and analyzing server logs.  
If you install successfully, open the XAMPP control panel, you should see this:
![image](pic/XAMPP_2.png)  
- To check XAMPP can work or not, you can tune on the Apache and MySQL:
![image](pic/XAMPP_3.png)  
- Click Admin under the Apache section in the control panel to check whether the default local web page can be accessed.
![image](pic/XAMPP_4.png)  
- If you see the page shown below, it means the server software is working properly.
![image](pic/XAMPP_5.png)  
- Next, check if MySQL is working properly. In the control panel, click Admin under the MySQL section to see if the MySQL dashboard opens successfully.
![image](pic/XAMPP_6.png)  
- And we have to set server's environment:
- First is change XAMPP's editer, original is Notepad, don’t open the file directly with it, as the code will appear all jumbled together.
- So we change it to VS code.
![image](pic/XAMPP_7.png)  
> [!WARNING]
>  You may face this problem  
> ![image](pic/XAMPP_error.jpg)  
> This issue is caused by insufficient permissions in XAMPP. Open Windows File Explorer and navigate to the file "C:\xampp\xampp-control.ini".
> Right-click the file and select Properties from the context menu.  
> ![image](pic/XAMPP_error_2.png)  
