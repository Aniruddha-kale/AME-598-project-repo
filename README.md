# AME-598-project-repo
In this project we are using a ESP32 microcontroller with a camera module and performing semantic segmentation on the images we get from the ESP32 camera.

Things you'll need:
1. ESP32 with camera module (https://usa.banggood.com/LILYGO-TTGO-T-Camera-ESP32-WROVER-with-PSRAM-Camera-Module-OV2640-Camera-0_96-Inch-OLED-p-1418433.html?imageAb=2&p=MA240439985285201910&cur_warehouse=CN&akmClientCountry=America&a=1670186430.6506&akmClientCountry=America)
2. Windows or mac pc/laptop with Arduino IDE installed (https://www.arduino.cc/en/software)
3. Git bash (https://git-scm.com/downloads)
4. CP210x USB to UART driver (https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads)

HOW TO:

1) Install and Launch the arduino IDE 
![IDE image](https://user-images.githubusercontent.com/112507554/205514885-9cba12ef-2222-4398-815a-ce8faa2e7448.png)

2) Add this to your boards: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
Open Arduino IDE >> Preferences >> Additional boards manager URLs
![Preferences img](https://user-images.githubusercontent.com/112507554/205515132-7c65a09f-0b9c-401e-85e9-01f01ec09f4f.png)

3) Install the USB to UART driver (https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads)
![usb uart driver img](https://user-images.githubusercontent.com/112507554/205515266-b0d3827f-5ae1-41d5-81d2-c3d6056e397c.png)

4) Install the ESP32 Library 
Open arduino IDE >> tools >> Boards manager >> Search "ESP32" and install the library
![esp32 library img](https://user-images.githubusercontent.com/112507554/205515509-14c51aaf-10c6-46d3-8f05-d2aa9293970b.png)

5) Now open the CameraWebServer folder and run the "CameraWebServer.INO" file and Connect ESP32 via USB cable and choose your port in Arduino IDE. make sure you have changed your wifi SSID and Password in the code.
 
6) Compile and run!!

7) Once the code is compiled and uploaded to the ESP32 open serial montor where you will find the IP address where you can get the video stream from the ESP32 camera
![serial monitor](https://user-images.githubusercontent.com/112507554/205517385-0ba2b9ea-cead-4781-81b3-a212ff5e6cb8.png)

![camera output](https://user-images.githubusercontent.com/112507554/205517396-138f440e-a90e-4baf-b04f-cb254e236034.png)

8) On your system clone the tfjs-models repo: https://github.com/tensorflow/tfjs-models

9) After cloning the repository open git bash and follow the instructions given here: https://github.com/tensorflow/tfjs-models/tree/master/deeplab/demo to run the semantic segmentation demo
![git bash img](https://user-images.githubusercontent.com/112507554/205517478-9422360d-4e37-4e4f-97ea-7e652a731300.png)

Now that the camera is working and the deeplab model is running we just need to take a photo and upload it on the website and get our results
![Screenshot (30)](https://user-images.githubusercontent.com/112507554/205517945-7f766124-5cf8-4852-bb2c-6d710fdbdb58.png)
