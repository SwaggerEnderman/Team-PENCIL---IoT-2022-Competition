# Team PENCIL presents
## The (TBD)
Is a device that is capable of detecting gas leaks, bleach leaks, and fires inside a home!
## The Team 
In order to make this device, we had to have a team that was both knowledgable as well as innovative, ##qualities that can be found in all of us. Dhiren was our main man for photographs and keeping track of our progress along the way. Ranvir was the guy for anything python related but he also crunched the numbers for our data analysis. Rushil was our hardware guy who also hanled most of the Arduino code. 
## The Hardware
This device contains a plethora of hardware parts that are required to make it the best that it can be!
### The Case
![IMG_4376-1](https://user-images.githubusercontent.com/80157888/182253272-2f10001b-65ea-4124-89e1-980ccb9a6097.jpeg)
The case for this device is a 3D printed dodecahedron with the bottom being printed out of black PLA and the top being printed out of gold PLA. It features a frosted acrylic front panel to be able to diffuse the lights from the LEDs softly and effectively for the user. 
### The Screen
![IMG_4413](https://user-images.githubusercontent.com/80157888/182253743-d0ebeaeb-e11c-4d85-bbd3-17bc2734fadc.jpeg)
This device features a 1.8" TFT Screen <img width="446" alt="image" src="https://user-images.githubusercontent.com/110428822/182688826-aaad2cc6-d710-4ca9-829b-5a3f8ebf94b6.png">that has a full color spectrum as well as a 128x160 screen resolution. It uses an SPI interface in order to connect to the ESP32 board and display the status of the home. Use of the Adafruit ST7735 library made the integration of this screen into our product much easier by providing easy to understand functions and actions. 
### The DFPlayerMini
![IMG_4406](https://user-images.githubusercontent.com/80157888/182258068-b4b3db27-2f83-4a02-8806-515f549ee598.jpeg)
The board above is a DFPlayerMini, a compact yet powerful driver board for a speaker. It uses a TF card in order to store and play MP3 files to a speaker and connects to the ESP32 via the RX and TX pins onboard.
### The Speaker
![IMG_4416](https://user-images.githubusercontent.com/80157888/182260272-a27e4e1b-34a4-4b83-98f6-b4d9a2faabfe.jpeg)
Paired with the DFPlayerMini is a 5W 4Ohm speaker from Logitech. Taken from a pair of Logitech S120 computer speakers, this speaker features a clear and crisp sound that makes it easy to hear anywhere in the house in the event of a need for evacuation. 
### The LEDs
![IMG_4408](https://user-images.githubusercontent.com/80157888/182253741-e4c3c389-4307-4755-b65d-f25eb8e1de3d.jpeg)
We used some WS2812B LEDs in order to display a color that would indicate the status of the home. These LEDS are super bright and use the full color spectrum! Integration is super simple via the use of the FastLED library which allows us to control the LEDs with a few simple commands.
### Data Collection
![Screenshot 2022-08-01 135024](https://user-images.githubusercontent.com/110428822/182686444-dcadcb55-4f79-48ac-8820-647a7fdab9e6.png)
![pasted image 0](https://user-images.githubusercontent.com/110428822/182686543-4df9b7d9-b759-4ca1-aede-1d7a8ede1c3b.png)
<img width="445" alt="image" src="https://user-images.githubusercontent.com/110428822/182688620-21195588-37e5-4401-b1fc-c2118fc0500c.png">
<img width="446" alt="image" src="https://user-images.githubusercontent.com/110428822/182688916-cefe0797-8184-499a-9580-e210988e397c.png">
<img width="445" alt="image" src="https://user-images.githubusercontent.com/110428822/182689042-5b61a33b-9604-42b7-a661-4ad1d1378612.png">
<img width="442" alt="image" src="https://user-images.githubusercontent.com/110428822/182689356-03593ff4-e1eb-45f8-ae82-a7149f37b29d.png">
<img width="447" alt="image" src="https://user-images.githubusercontent.com/110428822/182689440-7a554042-d7b4-4c7f-b1fa-2de0c7abc8b2.png">
<img width="446" alt="image" src="https://user-images.githubusercontent.com/110428822/182689560-1111e720-0b58-4ea1-8132-20d772a814b7.png">
![Uploading image.png…]()
