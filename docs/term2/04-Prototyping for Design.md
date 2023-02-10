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

While testing out the final materials the press fit was right on point for the cat but not so much for the airplane I also printed out on cardboard. This was because the model was too small and the material was not rigid enough. For the future I would love to explore using laster cutting for exhibit design mixing engraving with cut parts using negative space for typography.

###**Micro challenge 4** Arduino challenge
xxxxxx
