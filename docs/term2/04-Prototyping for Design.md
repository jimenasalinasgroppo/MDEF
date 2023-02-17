---
hide:
    - toc
---

# Prototyping For Design

## Week 1 - Day 1

Today Victor told us about microchips and the specific parts behind it. The highlight for me was learning that there were layers of communication that could be closest to the hardware and therefore most technical and then there were others that are closest to the user and therefore more accessible to humans, such as the chat prompts of GPT-3.


###**Micro challenge 1** Learning to activate music with a buzzer using our electronic kit.

This was my first time operating Arduino by myself. In Tech beyond the myth I worked with experts on my team so I was in charge of the communications aspect. Wen lent me here Arduino Uno which was a great starting point because its especially designed to teach children in high school to approach Arduino.

I started looking at open source libraries with different music tracks, such as Harry Potter, Ed Sheeran songs and The Pink Panther theme song. Marielle helped me iterate certain numbers on the code to get the code tu run properly on my computer.

> This is the code I inputted into Arduino. Saving it for future documentation.
// Copyright (c) 2022 HiBit <https://www.hibit.dev>
// -------------------------------------------------#include "pitches.h" #define BUZZER_PIN 8
int REST = 0;
int melody[] = {
  REST, REST, REST, NOTE_DS4,
  NOTE_E4, REST, NOTE_FS4, NOTE_G4, REST, NOTE_DS4,
  NOTE_E4, NOTE_FS4,  NOTE_G4, NOTE_C5, NOTE_B4, NOTE_E4, NOTE_G4, NOTE_B4,   
  NOTE_AS4, NOTE_A4, NOTE_G4, NOTE_E4, NOTE_D4,
  NOTE_E4, REST, REST, NOTE_DS4,
    NOTE_E4, REST, NOTE_FS4, NOTE_G4, REST, NOTE_DS4,
  NOTE_E4, NOTE_FS4,  NOTE_G4, NOTE_C5, NOTE_B4, NOTE_G4, NOTE_B4, NOTE_E5,
  NOTE_DS5,   
  NOTE_D5, REST, REST, NOTE_DS4,
  NOTE_E4, REST, NOTE_FS4, NOTE_G4, REST, NOTE_DS4,
  NOTE_E4, NOTE_FS4,  NOTE_G4, NOTE_C5, NOTE_B4, NOTE_E4,…
[1:57 p. m., 2/2/2023] Jimena: 2, 16, 16, 16, 16,
  4, 4,
  4, 8, 8, 8, 8, 8, 8,
  16, 8, 16, 8, 16, 8, 16, 8,   
  16, 16, 16, 16, 16, 2
};
void setup()
{
  pinMode(BUZZER_PIN, OUTPUT);
}
void loop()
{
  int size = sizeof(durations) / sizeof(int);
  for (int note = 0; note < size; note++) {
    //to calculate the note duration, take one second divided by the note type.
    //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
    int duration = 1000 / durations[note];
    tone(BUZZER_PIN, melody[note], duration);
  //to distinguish the notes, set a minimum time between them.
    //the note's duration + 30% seems to work well:
    int pauseBetweenNotes = duration * 1.30;
    delay(pauseBetweenNotes);
      //stop the tone playing:
    noTone(BUZZER_PIN);
  }
}

![](../images/MT02/arduino1.jpg)
> Computer screenshot trying to play around with the code.

<iframe src="https://drive.google.com/file/d/1B-k_0CPGA_EUfufSy7-iKUgSR2F0h0jh/preview" width="640" height="480" allow="autoplay"></iframe>
> Experiments with music playing with Arduino Uno.

<iframe src="https://drive.google.com/file/d/10qI70r5I5w05KhABOjRGJ7F32T0jfZ_8/preview" width="640" height="480" allow="autoplay"></iframe>
> Experiments with music playing with Arduino Uno.

## Week 1 - Day 2

Today Eduardo taught us more about modelling and 3D models. He started by introducing terminology such as pixels vs vectors and going to basics allowed all of us to start with a clear mind.

One of the technical highlights for me was learning the importance of reducing image file sizes when uploading them to a website and being mindful of the ecological impact of not doing this.

###**Micro challenge 2.1** Parametrizing a croissant

I asked Chat GPT3 to parametrize a croissant since I have zero experience with modeling and 3D software besides 3Ds max when I was doing an animation class on product advertising.

First I used Noun Project to look for 2D croissant vectors. I then looked for open Rhino libraries that would allow me to look for different croissant models. I downloaded one that looked the most simple and opened it up on Rhino.

![](../images/MT02/croissant.png)

###**Micro challenge 2.2** Create a 3D design based on algorithmic thinking of any object or concept you like.

This was very exciting for me because I have zero experience modelling but the tools are very accesible. I was interested in exploring how to do 3D models of illustrations and logotypes and deep dive on that a bit more. I really like the work of Cabeza Patata, an illustration collective that does 3D renderings of illustrations.

The software I chose was Blender, I wanted to get familiar with the tool and saw there was a very big internet community offering free tutorials. I started first watching introductory tutorials that showed me keyboard shortcuts and the logic behind the tool.

![](../images/MT02/render1.png)

I wanted to create a 3D version of a logotype I had created for a client last year. I chose that image because the shape is pretty simple and would have a potential use if I sent it back to the client.

I made this video outlining the end result and sharing a bit of my process. I learned to use the Boolean tool as a means to cut shapes inside the 3D model. The logic to me was very familiar as this is a technique I used when playing around with 2D vectors and typography.

I am really content with the end result even though I know it is quite basic. This made me aware that my interest in 3D modeling is more connected to illustration and branding rather than to engineering or making products.

I also tried to input "3D render letter M" on stable diffusion to see how the AI generated models looked like and how much they could serve me for this purpose.

<iframe src="https://drive.google.com/file/d/1cpFjbrwoYZcdUgm_nwvtEMNkgJIRbuMJ/preview" width="640" height="480" allow="autoplay"></iframe>

<iframe src="https://drive.google.com/file/d/1wUheQw-FMzn4cT79XZlqX_pWJ67tQQ-C/preview" width="640" height="480" allow="autoplay"></iframe>

<div style="position: relative; padding-bottom: 64.63195691202873%; height: 0;"><iframe src="https://www.loom.com/embed/a7195a10f0344416b72c9196f8e5258a" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Week 2 - Day 1

Today we learned about laser cutting and vinyl cutting. What resonated with me most was the application of these techniques for building installations and communicating ideas in spaces. Using pens with the vinyl cutter was also incredible, a way to mix an analog and traditional technique with the digital.

###**Micro challenge 3** Create a parametric model and print it.
To explore laser cutting press-fit for the first time I chose to build out of an existing file of a cat. I then modified the file size a bit to fit the laser cut machine and added my name to personalize the cat.

What was hardest of the process was setting up the properties on the laser cut machine to have the correct scale, position the laser in the right corner and understanding the colors for engraving and cutting. I set up the file with Wen and Carolina and we needed to ask Eduardo and Josep for help a couple of times. We used some spare cardboard that had already been used for our initial prototypes before using a fancier cardboard for the end result.

![](../images/MT02/cat2.jpeg)

While testing out the final materials the press fit was right on point for the cat but not so much for the airplane I also printed out on cardboard. This was because the model was too small and the material was not rigid enough. For the future I would love to explore using laster cutting for exhibit design mixing engraving with cut parts using negative space for typography.

![](../images/MT02/cat.jpeg)

## Week 2 - Day 2
We learned about inputs and outputs from Victor. It was very inspiring to learn how sensors such as GPS actually work and to see the potential of using sensors in fields such as biology where electronics has not been very funded or investigated much before.

I also enjoyed learning about DIY communities in Japan where making your own input and output systems is a great way to also combat private corporations using personal data for their own gain. Some questions asked during class that resonate with me: Why is Alexa so cheap if the investment for its development was so expensive? Answer: potentially they want to aim for the most quantity of Alexa's per household to gain our data and use that for profit.

###**Micro challenge 4** Arduino challenge
For this challenge I came to IAAC with Carolina, Wen, Sami and Josephine on Friday. We tried to individually set up our Arduinos to either light up the LED with the switch and to use the sensor correctly on a separate board.

We realized this task would take us much more time than we initially thought. I worked with Carolina trying to connect the switch to the LED light and were succesful for a period of time but then the Arduino stopped working. We tried plugging and re plugging everything but it didn't work again. Finally we got the board to keep working.

![](../images/MT02/arduino2.jpeg)

<iframe src="https://drive.google.com/file/d/1kGEJIMOf4V4TCAQaPAhjd-58WySkgSfi/preview" width="640" height="480" allow="autoplay"></iframe>

> **This was the code we used to get the output to work correctly (LED light).**
/*
 Button
 Turns on and off a light emitting diode(LED) connected to digital pin 13,
 when pressing a pushbutton attached to pin 2.
The circuit:
 - LED attached from pin 13 to ground through 220 ohm resistor
 - pushbutton attached to pin 2 from +5V
 - 10K resistor attached to pin 2 from ground
 - Note: on most Arduinos there is already an LED on the board
   attached to pin 13.
 created 2005
 by DojoDave <http://www.0j0.org>
 modified 30 Aug 2011
 by Tom Igoe
 This example code is in the public domain.
 https://www.arduino.cc/en/Tutorial/BuiltInExamples/Button
*/
// constants won't change. They're used here to set pin numbers:
const int buttonPin = 14;  // the number of the pushbutton pin
const int ledPin = 13;    // the number of the LED pin
const int buttonPin = 33;  // the number of the pushbutton pin
const int ledPin = 13;    // the number of the LED pin
const int ldrPin = A3;  
int ldrValue = 0; // luminosity
int start = 0;  // time starts counting
bool prevstate; // variable to evaluate previous state of the measurement
bool state;  // variable for assessing the status of point or dash
int buttonState = 0;  // variable for reading the pushbutton status
char punto = '.';
char raya = '-';
String letters[27]={
".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ".---", "-.-", ".-..", "--", "-.", "---", ".--.", "--.-", ".-.", "...", "-", "..-", "...-", ".--", "-..-", "-.--", "--..",  
};
void setup() {
 Serial.begin(9600);
 // initialize the LED pin as an output:
 pinMode(ledPin, OUTPUT);
 // initialize the pushbutton pin as an input:
 pinMode(buttonPin, INPUT);
}
void loop() {
 // read the state of the pushbutton value:
 buttonState = digitalRead(buttonPin);
 // check if the pushbutton is pressed. If it is, the buttonState is HIGH:
 if (buttonState == HIGH) {
   // turn LED on:
   digitalWrite(ledPin, HIGH);
![](../images/MT02/arduino3.jpeg)
<iframe src="https://drive.google.com/file/d/1o328u2SyitJx4OLxxbWRUyOrb4B-2Kx-/preview" width="640" height="480" allow="autoplay"></iframe>

## Week 3 - First Fab Lab challenge

This week I worked with Ariel and Wen to develop a physical product that would allow us to engage with children's perceptions in relation to 3 different fields: climate change, gender equality and mental health. We were inspired by analog data visualizations and an exercise we did with Holon during the Community Engagement week where we had to physically move our body along a spectrum to show how we felt in regards to certain topics.

One of the highlights for me was how fast we aligned on the subject matter and concept of the proposal. As early feedback we were suggested to incoporate electronics to our product that would be fabricated mostly using laser cutting. We used the first day to brainstorm some ideas that would not be time consuming and would above all be very meaningful for both the product and the facilitation behind it.

My participation in the project was primarily in designing the concept and MVP in digital format, looking at how the user interaction would work inside a classroom and how would the use of the Perception Board work integrating the cards, questions and the x and y axis. I then designed the question cards, itrating the content itself so it would be more understandable by children. My role was also to help set up the laser cutting and help Ariel and Wen finalize Rhino file details and pasting the parts of the final piece together with glue.

We will test the product with the school we previously worked but this time with older children since the exercise requires more cognitive skills and debate capabilities from them.

Some learnings that emerged from this week:
- **Electronics require a lot of time and that should be reflected on the planning side of managing time.** Colored LED lights also use different resistors and when lighting up many LEDs on one same product the amount of power is something to take into account.
- **When making different prototypes, take notes of changes in materials, design files and extra pieces you will need for next time.** For instance, by making the cardboard design we realized we need a card holder, some way to transport the board and a taller structure to hide the Arduino set up.
- **Laser cutting is also very time-sensitive** Make sure that happens earlier on you work flow because laser cutting two wooden boards can take over an hour.
- **Early alignment is key.** Had we not aligned on Tuesday on the output and key concept we would not have had time to fail early building the actual product and iterating.

I am looking forward to using our Perception board with teenagers and seeing how this project can also evolve in designing DIY tools for teachers to facilitate participatory processes with children and teenagers.

[Project repo](https://github.com/wenqianchua/microchallenge-01)
