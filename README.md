# Team PENCIL presents
## The Sharpener
The Sharpener is a device that is capable of detecting gas leaks, bleach leaks, and fires inside a home and is designed to sharpen the homeowners senses. This is for homeowners to let them know if there is a leak or fire in their house.
## Our Plan
Our plan was to make a device that can detect harmful substances if they are not contained. The first thing we did was brainstorm possible ideas we could do and ended up deciding on the device we're doing right now. After brainstorming, we came up with a design for the case. After we came up with the design of the case, we printed the parts of the case and decided what hardware we were going to use. Then we started programming. After we finished most of the programming, we started running tests for data. After all of that we finished programming the speaker and lights and ran our last test for data.
### The Team Log
6/23 Brainstorming Session

6/24 Cadding and 3D Printing

6/25 3D Printing

6/26 Sanding and Assembling Most of The Case

6/27 Programming and Working on Case

6/28 Planning

6/30 Unpackaging and Testing New parts

7/1 Still Testing out New Parts

7/5 Programming Speaker and OLED Screen

7/20 Assemble Case and Coding

7/21 - 8/5 Coding, Testing, Analyzing, Github

## The Team 
![IMG_4538](https://user-images.githubusercontent.com/80157888/183225542-656aaa66-81d4-4144-b4ba-264d6ad92927.JPG)
In order to make this device, we had to have a team that was knowledgable as well as innovative and helpful, qualities that can be found in all of us. Dhiren was our main man for photographs and keeping track of our progress along the way. Ranvir was the guy for anything python related but he also crunched the numbers for our data analysis. Rushil was our hardware guy who also handled most of the Arduino code. 
## The Hardware
### The Case
![IMG_4376-1](https://user-images.githubusercontent.com/80157888/182253272-2f10001b-65ea-4124-89e1-980ccb9a6097.jpeg)
The case for this device is a 3D printed dodecahedron with the bottom being printed out of black PLA and the top being printed out of gold PLA. It features a frosted acrylic front panel to be able to diffuse the lights from the LEDs softly and effectively for the user. 
### The Screen
![IMG_4413](https://user-images.githubusercontent.com/80157888/182253743-d0ebeaeb-e11c-4d85-bbd3-17bc2734fadc.jpeg)
This device features a 1.8" TFT Screen that has a full color spectrum as well as a 128x160 screen resolution. It uses an SPI interface in order to connect to the ESP32 board and display the status of the home. Use of the Adafruit ST7735 library made the integration of this screen into our product much easier by providing easy to understand functions and actions. 
### The DFPlayerMini
![IMG_4406](https://user-images.githubusercontent.com/80157888/182258068-b4b3db27-2f83-4a02-8806-515f549ee598.jpeg)
The board above is a DFPlayerMini, a compact yet powerful driver board for a speaker. It uses a TF card in order to store and play MP3 files to a speaker and connects to the ESP32 via the RX and TX pins onboard.
### The Speaker
![IMG_4416](https://user-images.githubusercontent.com/80157888/182260272-a27e4e1b-34a4-4b83-98f6-b4d9a2faabfe.jpeg)
Paired with the DFPlayerMini is a 5W 4Ohm speaker from Logitech. Taken from a pair of Logitech S120 computer speakers, this speaker features a clear and crisp sound that makes it easy to hear anywhere in the house in the event of a need for evacuation. 
### The LEDs
![IMG_4408](https://user-images.githubusercontent.com/80157888/182253741-e4c3c389-4307-4755-b65d-f25eb8e1de3d.jpeg)
We used some WS2812B LEDs in order to display a color that would indicate the status of the home. These LEDS are super bright and use the full color spectrum! Integration is super simple via the use of the FastLED library which allows us to control the LEDs with a few simple commands.

## The Overall Circuit
For times sake, we were unable to create a full blown circuit diagram but below are picture of the circuit.

![IMG_4546](https://user-images.githubusercontent.com/80157888/183226671-86e9cd09-3144-45f2-9a52-09c77b40a09a.JPG)
![IMG_4547](https://user-images.githubusercontent.com/80157888/183226672-5f714dbe-1c49-4fc3-9041-252ee2a79e49.JPG)

## The Data Collection
Our sensor detects different gases by using thresholds and boundaries that we created for the gas resistivity so when the values fell under these boundaries/threseholds it would run the alert code. To determine these thresholds and boundaries we have to collect data of the gases and create the thresholds after analyzing the data. We used two heater profiles, HP-354 and HP-411, and we decided to use the one that we liked the most or appealed to us in our final code the most but we ran trials and data collection with both heat profiles. We measured the gas resitivity of the room, the smoke emitted from fire, the smell emitted from gasoline, and the smell emitted from bleach. We decided to measure normal room gas just to compare our data and see the differences, while we decided to use the other gases as they are the harmful to a household due to fumes. To collect our data we ran python code and used the serial monitor to collect values. After evaluating both we decided to use the serial monitor values as they seemed easier to read and easier to build our threseholds around. 

![IMG_1141](https://user-images.githubusercontent.com/110428822/183228274-d330e679-f2fd-49d3-af7b-70c6bbcbb968.jpg)

### Excel Graphs
<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182688620-21195588-37e5-4401-b1fc-c2118fc0500c.png">

For the normal room temperature atmosphere, we saw after the first step the gas resistivity spikes up majorly but gradually decreases from 7000/8000 to 2000/3000 which then after the values decrease to around 200 and continue to decrease until step 8, which then they increase to 100. After doing many experiments we figured that the gases in each room differ a lot so we decide to record values in the same room. The purpose of the Hp-354 normal readings is to compare them to the other gases and other heat profiles. It also known as the 'constant' or 'independant' reading.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182690124-f2b63ef4-6e42-4ca4-aeed-609cad2960e0.png">

For the bleach the trend and values are very similar to the normal readings, the only difference being that the readings for the bleach is slightly higher when compared to the normal values, which would mean we would have to keep our thresholds for the bleach very small in order to prevent overlapping with the normal values and causing a false alarm. The jump from step 2 to step 3 was much steeper for the bleach compared to the normal values. 

<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182690384-f9c48e31-42d3-4899-a970-e61183c14f8b.png">

The difference in the gas values when compared with the bleach and normal values is that it's significantly smaller which means our thresholds were able to be a little more lenient. Another interesting thing we found is these values were actually higher than values for the fire, which we didnt expect as we thought they would be incredibly similar. The jump from step 2 to step 3 was also much smaller compared to the bleach.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182690454-f659a307-3ba5-4a50-9804-883f96e7e804.png">

The fire has higher values compared to the gas but lower values compared to the bleach, so it's basically in the middle of these two. Measuring the fire was quite difficult because we had to start the fire, then choke it, then record the values using the leftover smoke, but the smoke would diminish pretty quick, so it would be hard for the sensor to read proper values, so it took multiple tries for us to get some reliable data we were able to use. The drops from step 2 to step 3 and step 3 to step 4 were also steeper than most of the other gases. 

<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182690651-4b36ec2a-1949-4c6d-9410-8b3f983b9183.png">

The heat profile HP-411 was significantly more different when compared HP-354 due to its higher starting heat and lower general heat values. Therefore the normal graph for HP-411 has a larger drop from step 1 to step 2 compared to HP-354.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182690713-3952e303-23fb-45b4-aa78-636890895f46.png">

The difference between Hp-411's values for bleach and Hp-354's values for bleach was that Hp-411 had lower values, but Hp-411's values for bleach was higher than the normal Hp-411. Hp-411 bleach was a bit more consistent than Hp-354 bleach. This might have happened because of environmental changes as well as the lower general heats that provided more consistency for measurenments. 

<img width="500" alt="image" src="https://user-images.githubusercontent.com/110428822/182690899-e512b0ab-6c38-4fbd-a077-a9d533f116c7.png">

Hp-411 fire values has a similar trend to bleach and normal gasses/atmosphere, but it has lower values than both. Hp-411 fire values were somewhat easier to record as after many trial with the Hp-354 fire values, we got the hang of it. The scale of the fire was significantly lower although when viewed on its own it looks very similar to the bleach and normal graphs.

(*Note - A main trend found throughout the heater profiles was the scale changed between the gases but not as much the general line trend)

### Python Graphs
These are our python graphs and they were helpful to somewhat until we found out that the graphs weren't as helpful to us as we needed them so we thought it was unecessary analyze them.
#### HP-354
![Screenshot 2022-08-01 150747](https://user-images.githubusercontent.com/110428822/183178385-a39f93a1-03f8-4f25-ab38-c60502f6a718.png)

![pasted image 0](https://user-images.githubusercontent.com/110428822/183179895-dff4eafc-1e56-48ce-afaa-a0c6399f0309.png)

![Screenshot 2022-08-01 135024](https://user-images.githubusercontent.com/110428822/183186130-df86e44d-33b8-4cab-ab5f-61860a251ca3.png)

#### HP-411
![Screenshot 2022-08-02 105006](https://user-images.githubusercontent.com/110428822/183183324-b08c11ec-672a-498f-a2cf-a4a42db36886.png)

![Screenshot 2022-08-02 105006](https://user-images.githubusercontent.com/110428822/183187809-cfc2d6d7-49f7-4713-b45c-da28b552115e.png)

![Screenshot 2022-08-03 135837](https://user-images.githubusercontent.com/110428822/183188406-0c8c6326-92b1-4b35-8267-fbe9edd51cc7.png)

## Code
For the code, we decided to split up the code into several functions that could be called when needed for simplicities sake. Below is an explanation of the functions of each function. 

(Line 1 - 66 is just libraries and definitions of variables for the code)

`void startupScreen()` - This function holds all of the code for the TFT Screen to print out our logo and company name on the screen upon boot. It gets called during `void setup()`.

`void initializeNTP()` - This function uses the NTP (Network Time Protocol) in order to connect to an NTP server and recieve time to display on our screen. It gets called during `void setup()`.

`void initializeBMESensor()` - This function initializes the BME680 and makes it ready for use whilst also setting oversampling and also returns error messages to the serial monitor for troubleshooting. It gets called during `void setup()`

`void initializeDFPlayerMini()` - This function sets up the DFPlayer Mini for use and also gives us updates on both errors as well as progress of the setup of the DFPlayer. It gets called during `void setup()`.

`void initializeLEDs()` - This function initializes the FastLED library, the library used for controlled the led strip we have inside of the case. It gets called during `void setup()`.

`void printTime()` - This function utilizes the TFT screen in tandem with the NTP in order to print the current time to the screen for the user's convenience. It gets called during `void loop()`.

`void measureGasResistance()` - This function uses the Adafruit BME680 library in order to set the heater profile and pull values. It then stores those values in variables that make it available for use later in the code. (*Note - For simplicity and times sake, we only used one heater profile -- HP-354 -- but we collected data for both HP-354 and HP-411) The function also prints out those values to the serial monitor for easy debugging. It gets called during `void loop()`.

`void detectGases()` - This function utilizes the previous heater profile values stored in those variables in order to detect one of three different types of household hazards -- a fire, a bleach leak, or a gasoline leak. Once it detects a hazard, the function will print the hazard on the screen while also changing the lights red and also playing a loud noise to alert the homeowner. In the case a hazard is not present, however, the screen will print "normal" and nothing will sound. It gets called during `void loop()`.

## The Development 
![image](https://user-images.githubusercontent.com/98428580/183228409-2770ede8-4380-4985-b211-ada69068bdbf.png)
![image](https://user-images.githubusercontent.com/98428580/183228418-d3aa5d8f-440d-4406-b200-fe19a27f4691.png)
![image](https://user-images.githubusercontent.com/98428580/183228424-bf494c11-1629-4666-a7f7-742735cfb2de.png)
![image](https://user-images.githubusercontent.com/98428580/183228426-23eed537-c573-4880-b036-6ea25fd84b85.png)
![image](https://user-images.githubusercontent.com/98428580/183228431-47c4cb3b-6c3d-49e6-ba3f-266a7c241ef6.png)
![image](https://user-images.githubusercontent.com/98428580/183228438-ecb43c6d-dc12-4a17-a873-2d59ec512701.png)
![image](https://user-images.githubusercontent.com/98428580/183228446-ce6f3397-e0b5-4f81-87a0-1fb9ce10e70f.png)
![image](https://user-images.githubusercontent.com/98428580/183228451-d292df7b-dcc6-48d9-a97d-478f500dff19.png)
![image](https://user-images.githubusercontent.com/98428580/183228459-91485294-c2eb-4428-a451-64680768a056.png)
![image](https://user-images.githubusercontent.com/98428580/183228465-8549be2d-b858-44d5-a4a0-2cce44610fb8.png)

## The Demo and Final Product

https://user-images.githubusercontent.com/80157888/183226086-66d02789-4ec0-4276-b159-bb05ae5ba8f8.mp4

https://user-images.githubusercontent.com/80157888/183227075-c47007af-25b0-4260-bb42-b11bf8e5b506.mp4


## The Challenges
One problem we had during data collection is that our sensor fell into the gasoline, so it would permanently read wrong values. In result of this, we had to get a new sensor and redo each trial because we figured that the new sensor would read different values from the previous one. Another issue is that this happened towards the end of the competition, so a lot of the testing had to be redone very quickly and it became quite challenging to work that fast. In the end, we made plans on what to do each day which helped us pace ourselves well enough to have this product finished on time. 

## The Conclusion
In conclusion, we are very proud of our device we made, as we also had a lot of fun making it. This device in the real world would be very helpful and will look aesthetic and pleasing.

